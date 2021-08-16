---
title: Atributo VML Eqn
description: Atributo VML Eqn
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae5872c29064f24a10b4a12c0d0e2a4ca4a200f79e295d60713fe56355f23aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655455"
---
# <a name="vml-eqn-attribute"></a>Atributo VML Eqn

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la ecuación utilizada por una fórmula. Lectura/escritura **Cadena**.

**Se aplica a**

[F](msdn-online-vml-f-element.md) (subelemento de [fórmulas)](msdn-online-vml-formulas-element.md)

**Sintaxis de etiquetas**

<v: *element* eqn=" *expression* ">

**Sintaxis de script**

*element* .eqn="*expression*"

*expresión* = *elemento*.eqn

**Comentarios:**

Las ecuaciones se definen mediante la evaluación de una expresión de texto que tiene la forma general de una operación seguida de hasta tres argumentos. Cada argumento puede ser de los siguientes tipos:

-   ajuste (por ejemplo, \# 2)
-   otra fórmula (por ejemplo, @2 )
-   números fijos (por ejemplo, 2)
-   valores predefinidos

En la tabla siguiente se definen las fórmulas que se pueden usar con los argumentos opcionales dados los nombres *v*, *p1* y *p2.* El patrón de fórmula es:

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Operación | Params | Exact  | Resultado                    | Descripción                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| Val       | 1      | Sí    | v                         | Define un valor de guía de otro valor.                                   |
| Sum       | 3      | Sí    | v + p1 : p2               | Se usa para sumar y restar.                                             |
| product   | 3      | Rondas | v \* p1/p2              | Se usa para la multiplicación y la división.                                          |
| mId       | 2      | (c)    | (v + p1)/ 2               | Average                                                                       |
| abs       | 1      | Sí    | abs(v)                    | Valor absoluto.                                                                |
| mín.       | 2      | Sí    | min(v,p1)                 | Valor menor de v y p1.                                                  |
| máx.       | 2      | Sí    | max(v,p1)                 | Valor mayor de v y p1.                                                 |
| if        | 3      | Sí    | v > 0 ? p1: p2        | Pruebas condicionales.                                                           |
| mod       | 3      | No     | sqrt(v^2 + p1^2 + p2^2)   | Valor de módulo.                                                                 |
| atan2     | 2      | No     | atan2(p1,v)               | Valor polar en grados \* 2^16 (fd units).                                     |
| sin       | 2      | No     | v \* sin(p1)              | Sin, argumento en grados \* 2^16 (fd [units](msdn-online-vml-units.md) ).     |
| cos       | 2      | No     | v \* cos(p1)              | Cos, argumento en grados \* 2^16 (fd [units](msdn-online-vml-units.md) ).     |
| cosatan2  | 3      | No     | v \* cos(atan2(p2,p1))    | Conserva la precisión completa en el cálculo intermedio.                           |
| sinatan2  | 3      | No     | v \* sin(atan2(p2,p1))    | Conserva la precisión completa en el cálculo intermedio.                           |
| sqrt      | 1      | No     | sqrt(v)                   | El resultado es positivo y se redondea hacia abajo.                                            |
| sumangle  | 3      | Sí    | v + p1 \* 2^16 + p2 \* 2^16 | v escalado en 2^16; p1 y p2 son grados.<br/>                            |
| ellipse   | 3      | No     | p2 \* sqrt(1-(v/p1)^2)    | Elipse.                                                                       |
| tan       | 2      | No     | v \* tan(p1)              | Tangente, argumento en grados \* 2^16 (fd [unidades](msdn-online-vml-units.md) ). |



 

Tenga en cuenta que la ecuación solo consta de operaciones y números; se omiten los símbolos matemáticos. Por ejemplo, la ecuación

eqn="sum 5 9 3"

produciría el equivalente de

5 + 9 - 3

para el valor devuelto de 11. Si faltan operandos, no se usa el valor . Por ejemplo,

eqn="sum 5 9"

produciría el equivalente de

5 + 9

y omitirían el operando que falta.

*Atributo estándar de VML*

**Ejemplo**

La fórmula siguiente produciría un resultado de 6 (la suma de ambos números divididos entre 2), que, si esta fuera la primera fórmula, podría recuperarse con el símbolo " @0 ".


```HTML
    <v:f eqn="mid 5 7"/>
```



 

