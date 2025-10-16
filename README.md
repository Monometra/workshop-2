# Test Navette

### Este es un simple algoritmo usando formulas y demas cave recalcar que yo lo hice solo porque mi compañero no me contacto en la pasada noche

---

## Explicacion del algoritmo

1. **Pide los datos de 10 personas:**
   - Nombre  
   - Edad (en años)  
   - Nivel alcanzado (`L`)  
   - Shuttle dentro del nivel (`S`)

2. **Valida los datos**  
   - La edad debe ser mayor que 0.  
   - El nivel debe ser mayor o igual a 1.  
   - El shuttle no puede ser negativo.

3. **Calcula la velocidad final** del participante:
   ```pseudocode
   V = 8 + 0.5 * L
   ```
   
> [!NOTE]
> Esta fórmula aproxima la velocidad final alcanzada según el nivel completado del test.
   

4. **Calcula dos tipos de VO₂ máx:**
   - **Fórmula simple:**  
     `VO₂_simple = 3.46 * V + 12.2`
   - **Fórmula de Léger:**  
     `VO₂_leger = 31.025 + (3.238 * V) - (3.248 * edad) + (0.1536 * V * edad)`

5. **Clasifica el rendimiento** usando el VO₂ simple:
   - Menos de **35:** Baja  
   - Entre **35 y 44.9:** Promedio  
   - Entre **45 y 54.9:** Buena  
   - Mayor o igual a **55:** Excelente  

6. **Muestra los resultados individuales**:
   - Nombre, edad, nivel, shuttle  
   - Velocidad final (V)  
   - VO₂ Simple  
   - VO₂ Léger  
   - Clasificación

7. **Calcula promedios grupales** al final:
   - Promedio del VO₂ simple  
   - Promedio del VO₂ Léger

---

## Ejemplo de resultado

```
Participante: Juan
Edad: 20 años
Nivel alcanzado: 8
Shuttle: 5
Velocidad final (V): 12.00 km/h
VO2 simple: 53.72 ml/kg/min
VO2 Léger: 49.33 ml/kg/min
Clasificación: Buena
```

Y al final del grupo:

```
Promedio VO2 simple: 45.87 ml/kg/min
Promedio VO2 Léger: 43.21 ml/kg/min
```

---

## Estructura básica del programa

```pseudocode
Para i ← 1 Hasta 10 Hacer
    Leer nombre, edad, nivel, shuttle
    Validar datos
    Calcular V
    Calcular VO2_simple y VO2_leger
    Clasificar rendimiento
    Mostrar resultados
    Acumular valores para promedio
FinPara
Mostrar promedios finales
```

---

## Formulas clave

| Calculo | Formula | Significado |
|----------|----------|-------------|
| Velocidad final | `V = 8 + 0.5 * L` | Aumenta medio km/h por nivel |
| VO₂ Simple | `3.46 * V + 12.2` | Estimación rápida de VO₂ |
| VO₂ Léger | `31.025 + (3.238 * V) - (3.248 * edad) + (0.1536 * V * edad)` | Fórmula más precisa del test original |

---

> [!TIP]  
> Puedes modificar el número de participantes cambiando el `Para i ← 1 Hasta 10` por una variable `n` que se lea al inicio del programa.

---
