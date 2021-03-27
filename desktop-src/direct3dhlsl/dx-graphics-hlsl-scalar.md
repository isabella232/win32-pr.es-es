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
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "103820882"
---
# <a name="scalar-types"></a>Tipos escalares


HLSL admite varios tipos de datos escalares:

-   **booleano** : true o false.
-   entero de bits con signo **int** -32.
-   entero de tipo **uint** -32 bits sin signo.
-   **DWORD** : entero sin signo de 32 bits.
-   valor de punto flotante de **16 bits.** Este tipo de datos solo se proporciona para la compatibilidad de lenguajes. Los destinos del sombreador de Direct3D 10 asignan a los tipos de datos float todos los tipos de datos de medio. No se puede usar un tipo de medio de datos en una variable global uniforme (use la marca/GEC si se desea esta funcionalidad).
-   valor de punto flotante de **tipo float** -32 bits.
-   valor de punto flotante de **doble** 64 bits. No se pueden usar valores de precisión doble como entradas y salidas de una secuencia. Para pasar valores de precisión doble entre los sombreadores, declare cada **Double** como un par de tipos de datos **uint** . A continuación, utilice la función [**asuint**](asuint.md) para empaquetar cada **Double** en el par de **uint** s y la función [**asdouble**](asdouble.md) para desempaquetar de nuevo el par de **uint** s en el **Double**.

A partir de Windows 8 HLSL también se admiten los tipos de datos escalares de precisión mínima. Los controladores de gráficos pueden implementar tipos de datos escalares de precisión mínima usando cualquier precisión mayor o igual que la precisión de bits especificada. Se recomienda no confiar en el comportamiento de compresión o ajuste que depende de la precisión subyacente específica. Por ejemplo, el controlador de gráficos puede ejecutar aritmética en un valor **min16float** con una precisión completa de 32 bits.

-   **min16float** : valor de punto flotante de 16 bits mínimo.
-   **min10float** : valor de punto flotante de 10 bits mínimo.
-   **min16int** : entero de 16 bits con signo como mínimo.
-   **min12int** : entero de 12 bits con signo como mínimo.
-   **min16uint** : entero de 16 bits sin signo mínimo.

Para obtener más información acerca de los literales escalares, vea [Grammar](dx-graphics-hlsl-appendix-grammar.md).



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10:<br/> En Direct3D 10, los siguientes tipos son modificadores para el tipo float.<br/>
<ul>
<li><strong>snorm Float</strong> - IEEE 32-bit signed: Float normalizado en el intervalo de 1 a 1, ambos inclusive.</li>
<li><strong>unorm Float</strong> - IEEE 32 bits sin signo: valor Float normalizado en el intervalo comprendido entre 0 y 1, ambos inclusive.</li>
</ul>
Por ejemplo, a continuación se muestra una declaración de variable Float normalizada con signo de 4 componentes.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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

HLSL también admite un tipo de **cadena** , que es una cadena ASCII. No hay operaciones ni Estados que acepten cadenas, pero los efectos pueden consultar los parámetros de cadena y las anotaciones.

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
* [Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)