🔹 Diferencia entre == y ===

== → compara valor (hace conversión de tipos automática)

=== → compara valor y tipo (NO convierte tipos)

✅ Ejemplo donde dan distinto:
console.log(5 == "5");   // true
console.log(5 === "5");  // false
📌 ¿Por qué?

== convierte "5" → número → 5 == 5 → true

=== compara número con string → distintos tipos → false

🔹 ¿Qué es la coerción de tipos?

Es cuando JavaScript convierte automáticamente o manualmente un valor de un tipo a otro.

🔸 Coerción implícita (automática)
console.log("5" + 2);   // "52"  (convierte 2 a string)
console.log("5" - 2);   // 3     (convierte "5" a número)
🔸 Coerción explícita (manual)
let numero = Number("10");
console.log(numero); // 10
🔹 Operadores lógicos (|| y &&)

No devuelven solo true/false, devuelven valores reales.

✅ Ejemplos:
console.log(false || "hola"); // "hola"
console.log("hola" && 0);     // 0
📌 ¿Cómo funcionan?

|| → devuelve el primer valor verdadero (truthy)

&& → devuelve el primer valor falso (falsy)

👉 Valores falsy: false, 0, "", null, undefined, NaN

🔹 Estructuras de control de flujo
🔸 if / else

Para decisiones simples

if (edad >= 18) {
  console.log("Mayor");
} else {
  console.log("Menor");
}

👉 Usalo cuando hay pocas condiciones

🔸 switch

Para múltiples opciones del mismo valor

switch (dia) {
  case 1:
    console.log("Lunes");
    break;
  case 2:
    console.log("Martes");
    break;
}

👉 Mejor cuando comparás una variable contra muchos valores

🔹 Operador ternario

Forma corta de un if

✅ Ejemplo:
let mensaje = edad >= 18 ? "Mayor" : "Menor";
🔁 Equivalente con if:
let mensaje;
if (edad >= 18) {
  mensaje = "Mayor";
} else {
  mensaje = "Menor";
}
🔹 Bucles
🔸 for (cuando sabés cuántas veces)
for (let i = 0; i < 5; i++) {
  console.log(i);
}
🔸 while (cuando no sabés cuántas veces)
let i = 0;

while (i < 5) {
  console.log(i);
  i++;
}
🔹 break y continue
🔸 break

Corta el bucle completamente

for (let i = 0; i < 5; i++) {
  if (i === 3) break;
  console.log(i);
}
// imprime: 0, 1, 2
🔸 continue

Salta una iteración

for (let i = 0; i < 5; i++) {
  if (i === 3) continue;
  console.log(i);
}
// imprime: 0, 1, 2, 4