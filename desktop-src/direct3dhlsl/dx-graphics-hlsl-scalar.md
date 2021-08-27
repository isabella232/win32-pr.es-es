---
title: Tipos escalares
description: Tipos escalares
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Tipos escalares HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7ddfbc679d95ca0a2c6fce0710b5de37f677fe0f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626731"
---
# <a name="scalar-types"></a>Tipos escalares


HLSL admite varios tipos de datos escalares:

-   **bool:** true o false.
-   **int:** entero de 32 bits con signo.
-   **uint:** entero de 32 bits sin signo.
-   **dword:** entero de 32 bits sin signo.
-   **half:** valor de punto flotante de 16 bits. Este tipo de datos solo se proporciona por compatibilidad de lenguaje. Los destinos de sombreador de Direct3D 10 asignan la mitad de los tipos de datos a tipos de datos float. No se puede usar un tipo de datos medio en una variable global uniforme (use la marca /Gec si se desea esta funcionalidad).
-   **float:** valor de punto flotante de 32 bits.
-   **double:** valor de punto flotante de 64 bits. No se pueden usar valores de precisión doble como entradas y salidas para una secuencia. Para pasar valores de precisión doble entre sombreadores, declare cada **double** como un par de tipos de datos **uint.** A continuación, use la función  [**asuint**](asuint.md) para empaquetar cada double en el par de **uint** s y la función [**asdouble**](asdouble.md) para desempaquetar el par de **uint** de nuevo en **el doble**.

A partir de Windows 8 HLSL también admite tipos de datos escalares de precisión mínima. Los controladores gráficos pueden implementar tipos de datos escalares de precisión mínima mediante cualquier precisión mayor o igual que la precisión de bits especificada. Se recomienda no basarse en el comportamiento de fijación o ajuste que depende de la precisión subyacente específica. Por ejemplo, el controlador de gráficos podría ejecutar operaciones aritméticas en un valor **min16float** con una precisión completa de 32 bits.

-   **min16float:** valor mínimo de punto flotante de 16 bits.
-   **min10float:** valor mínimo de punto flotante de 10 bits.
-   **min16int:** entero de 16 bits con signo mínimo.
-   **min12int:** entero de 12 bits con signo mínimo.
-   **min16uint:** entero de 16 bits sin signo mínimo.

Para obtener más información sobre los literales escalares, vea [Grammar](dx-graphics-hlsl-appendix-grammar.md).



<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10:<br/> En Direct3D 10, los siguientes tipos son modificadores del tipo float.<br/>
<ul>
<li><strong>snorm float</strong> - Float con firma de IEEE de 32 bits normalizado en el intervalo de -1 a 1, ambos inclusive.</li>
<li><strong>unorm float</strong> - Flotante sin signo ieee de 32 bits sin signo en el intervalo de 0 a 1, ambos inclusive.</li>
</ul>
Por ejemplo, esta es una declaración float-variable con firma normalizada de 4 componentes.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a>Tipo de cadena

HLSL también admite un **tipo de** cadena, que es una cadena ASCII. No hay operaciones ni estados que acepten cadenas, pero los efectos pueden consultar parámetros de cadena y anotaciones.

## <a name="example"></a>Ejemplo

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a>Vea también



* [Declarar tipos escalares](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [Tipos de datos (HLSL de DirectX)](dx-graphics-hlsl-data-types.md)
