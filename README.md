# Motor_de_Inferencia_en_Python
En esta actividad construirás desde “cero” un sistema experto funcional para diagnóstico de problemas técnicos en computadoras. No existe el uso de ninguna librería externa: sólo Python puro con listas, diccionarios, conjuntos y funciones.


### 1) Diferencia principal entre un sistema experto y un programa de software tradicional
- El sistema experto imita el razonamiento humano aplicando reglas y conocimientos.  
- El software tradicional ejecuta instrucciones fijas sin interpretar ni aprender del contexto.

---

### 2) ¿Por qué se dice que los sistemas expertos tienen conocimiento separado de su motor de razonamiento? ¿Cuál es la ventaja?
- Porque el motor de inferencia está separado de la base de conocimiento (hechos y reglas).  
- **Ventaja:** Permite actualizar el conocimiento sin reprogramar el motor. Así el sistema es más flexible y fácil de mantener.

---

### 3) ¿Qué es la base de hechos y en qué se diferencia de la base de conocimiento?
- **Base de hechos:** Contiene datos específicos de la situación actual.  
- **Base de conocimiento:** Contiene reglas generales y expertas.  
- **Diferencia:** La base de hechos cambia constantemente; la base de conocimiento es más estable.

---

### 4) ¿Qué significa que un sistema experto pueda "explicar su razonamiento"? ¿Por qué esto es importante en medicina o derecho?
- Significa que el sistema puede mostrar qué reglas aplicó y por qué llegó a una conclusión.  
- **Importancia:** En medicina y derecho se necesita transparencia y justificación para que el profesional confíe en la recomendación y pueda defenderla.

---

### 5) ¿Por qué fracasaron comercialmente los sistemas expertos en los años 90? (3 razones)
1. Altos costos de desarrollo y mantenimiento (difícil capturar conocimiento experto).  
2. Limitaciones tecnológicas (hardware y software poco potentes para manejar grandes bases de reglas).  
3. Rigidez y falta de escalabilidad (no podían adaptarse fácilmente a nuevos contextos o aprender automáticamente).

---

### 6) Regla:  
`SI (fiebre AND tos) OR perdida_olfato ENTONCES sospecha_covid`  
Hechos: `{fiebre=True, tos=False, perdida_olfato=True}`  

- Evaluación: `(True AND False) OR True = False OR True = True`.  
- **Resultado:** La regla se activa porque la condición de pérdida de olfato es verdadera.

---

### 7) Tabla de verdad para (A AND NOT B) OR (NOT A AND B)

| A | B | A AND NOT B | NOT A AND B | Resultado |
|---|---|-------------|-------------|-----------|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 1 | 0 | 1 |
| 1 | 1 | 0 | 0 | 0 |

👉 Es la expresión de la **XOR** (exclusiva).

---

### 8) Diferencia entre encadenamiento hacia adelante y hacia atrás
- **Hacia adelante:** Parte de los hechos y aplica reglas hasta llegar a conclusiones.  
  - Ejemplo: En un sistema médico, ingresas síntomas y el sistema deduce posibles enfermedades.  
- **Hacia atrás:** Parte de una hipótesis y busca hechos que la confirmen.  
  - Ejemplo: En derecho, si se sospecha de fraude, el sistema busca pruebas que validen esa hipótesis.

---

### 9) Diseña 3 reglas IF-THEN para asesorar estudiantes sobre qué lenguaje aprender primero
1. SI objetivo = desarrollo web → ENTONCES recomendar **JavaScript**.  
2. SI objetivo = análisis de datos → ENTONCES recomendar **Python**.  
3. SI objetivo = desarrollo de videojuegos → ENTONCES recomendar **C#**.

---

### 10) Red de inferencia correspondiente a las 3 reglas

---

### 11) Problema de diseño si dos reglas tienen mismas condiciones pero conclusiones diferentes
- **Problema:** Conflicto de reglas → el sistema no sabe cuál conclusión aplicar.  
- **Solución:**  
  - Definir prioridades o pesos en las reglas.  
  - Usar un mecanismo de resolución de conflictos (ej. elegir la regla más específica o la más reciente).  
  - Incluir un experto humano para validar en casos ambiguos.


