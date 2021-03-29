---
title: Atributo eqn de VML
description: Atributo eqn de VML
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da00084a825147c6f8a05f503e5ee2679f40e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359400"
---
# <a name="vml-eqn-attribute"></a>Atributo eqn de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la ecuación usada por una fórmula. Lectura/escritura **Cadena**.

**Se aplica a**

[F](msdn-online-vml-f-element.md) (subelemento de [fórmulas](msdn-online-vml-formulas-element.md))

**Sintaxis de etiquetas**

<v: *Element* eqn = " *expresión* " >

**Sintaxis de script**

*Element* . eqn = "*expresión*"

*expresión* = de *elemento*. eqn

**Comentarios:**

Las ecuaciones se definen mediante la evaluación de una expresión de texto que tiene la forma general de una operación seguida de hasta tres argumentos. Cada argumento puede ser de los siguientes tipos:

-   ajuste (por ejemplo, \# 2)
-   otra fórmula (por ejemplo, @2 )
-   números fijos (por ejemplo, 2)
-   valores predefinidos

En la tabla siguiente se definen las fórmulas que se pueden usar con los argumentos opcionales dados los nombres *v*, *P1* y *P2*. El patrón de fórmulas es:

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Operación | Params | Exact  | Resultado                    | Descripción                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| Val       | 1      | sí    | v                         | Define un valor de guía de otro valor.                                   |
| Sum       | 3      | sí    | v + P1-P2               | Se utiliza para sumar y restar.                                             |
| product   | 3      | baza | v \* P1/P2              | Se utiliza para la multiplicación y la división.                                          |
| mId       | 2      | unidad    | (v + P1)/2               | Average                                                                       |
| abs       | 1      | sí    | ABS (v)                    | Valor absoluto.                                                                |
| min.       | 2      | sí    | mín. (v, P1)                 | El valor menor de v y P1.                                                  |
| max       | 2      | sí    | máx. (v, P1)                 | El valor mayor de v y P1.                                                 |
| if        | 3      | sí    | v > 0? P1: P2        | Pruebas condicionales.                                                           |
| mod       | 3      | no     | sqrt (v ^ 2 + P1 ^ 2 + P2 ^ 2)   | Valor de módulo.                                                                 |
| atan2     | 2      | no     | ATAN2 (P1, v)               | Valor polar en grados \* 2 ^ 16 (unidades FD).                                     |
| sin       | 2      | no     | \*sin v (P1)              | Sin, argumento en grados \* 2 ^ 16 ( [unidades](msdn-online-vml-units.md) FD).     |
| cos       | 2      | no     | v \* cos (P1)              | Cos, argumento en grados \* 2 ^ 16 ( [unidades](msdn-online-vml-units.md) FD).     |
| cosatan2  | 3      | no     | v \* cos (ATAN2 (P2, P1))    | Conserva la precisión completa en el cálculo intermedio.                           |
| sinatan2  | 3      | no     | \*sin v (ATAN2 (P2, P1))    | Conserva la precisión completa en el cálculo intermedio.                           |
| sqrt      | 1      | no     | sqrt (v)                   | El resultado es positivo y se redondea hacia abajo.                                            |
| sumangle  | 3      | sí    | v + P1 \* 2 ^ 16 + P2 \* 2 ^ 16 | v escalada por 2 ^ 16; P1 y P2 son grados.<br/>                            |
| ellipse   | 3      | no     | P2 \* sqrt (1-(v/P1) ^ 2)    | Puntos.                                                                       |
| tan       | 2      | no     | v \* tan (P1)              | Tangente, argumento en grados \* 2 ^ 16 ( [unidades](msdn-online-vml-units.md) FD). |



 

Tenga en cuenta que la ecuación solo consta de operaciones y números; se omiten los símbolos matemáticos. Por ejemplo, la ecuación

eqn = "SUM 5 9 3"

produciría el equivalente de

5 + 9-3

para el valor devuelto de 11. Si faltan operandos, no se utiliza el valor. Por ejemplo,

eqn = "SUM 5 9"

produciría el equivalente de

5 + 9

y omitirían el operando que falta.

*Atributo estándar de VML*

**Ejemplo**

La siguiente fórmula produciría un resultado de 6 (la suma de ambos números divididos por 2), que, si se trata de la primera fórmula, podría recuperarse con el símbolo " @0 ".


```HTML
    <v:f eqn="mid 5 7"/>
```



 

