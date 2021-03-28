---
title: Tipo de muestra
description: Use la siguiente sintaxis para declarar el estado de la muestra, así como el estado de la comparación de muestra.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Tipo de muestra HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe3cd51c81617632d240dd06df5c8f61b103bf91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077778"
---
# <a name="sampler-type"></a>Tipo de muestra

Use la siguiente sintaxis para declarar el estado de la muestra, así como el estado de la comparación de muestra.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10 y versiones posteriores:<br/> Esta es la sintaxis de una muestra en Direct3D 9.<br/> 
<table>
<tbody>
<tr class="odd">
<td><em>nombre</em>de muestra  =  <em>SamplerType</em>{Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La sintaxis de una muestra en Direct3D 10 y versiones posteriores se cambia ligeramente para admitir objetos de textura y matrices de muestra.</p>

<table>
<tbody>
<tr class="odd">
<td><em>SamplerType nombre [índice]</em>{[<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>muestras
</dt> <dd>

Solo Direct3D 9. Palabra clave required.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre de la variable de muestra.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Ajustar\]*
</dt> <dd>

Solo Direct3D 10 y versiones posteriores. Tamaño de matriz opcional; un entero positivo mayor o igual que 1.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*
</dt> <dd>

\[en \] el tipo de muestra, que es uno de los siguientes: *Sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *\_ State Sample*, *SamplerState*.



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10 y versiones posteriores:<br/> Direct3D 10 y versiones posteriores admiten un tipo de muestra adicional: *SamplerComparisonState*.<br/> |



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*\_ variable de textura*>;
</dt> <dd>

Solo Direct3D 9. Una variable de textura. La palabra clave *Texture* es obligatoria en el lado izquierdo; el nombre de la variable pertenece al lado derecho de la expresión dentro de los corchetes angulares.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*nombre del estado \_ = \_ valor de estado*
</dt> <dd>

\[en \] asignaciones de estado opcionales. La parte izquierda de una asignación es un nombre de estado, el lado derecho es el valor de estado. Todas las asignaciones de estado deben aparecer dentro de un bloque de instrucciones (entre llaves). Cada instrucción se separa con un punto y coma. En la tabla siguiente se enumeran los nombres de estado posibles.


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



El lado derecho de cada expresión es el valor asignado a cada Estado. Consulte la [**estructura \_ \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) de la muestra de D3D11 para ver los valores de estado posibles para Direct3D 11. Hay una relación de 1 a 1 entre los nombres de estado y los miembros de la estructura. Consulte el ejemplo siguiente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se implementa un efecto, el estado de muestra es uno de los diversos tipos de estado que puede necesitar configurar en la canalización para la representación. Para obtener una lista de todos los Estados posibles que se pueden establecer en un efecto, vea:

-   Direct3D 10 usa [grupos de Estados](/windows/desktop/direct3d10/d3d10-effect-states).
-   Direct3D 9 usa [Estados](/windows/desktop/direct3d9/effect-states)individuales.

## <a name="example"></a>Ejemplo



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10:<br/> Este es un ejemplo parcial de una muestra de Direct3D 9 de <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">ejemplo de BasicHLSL</a>.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p>Este es un ejemplo parcial de una muestra de Direct3D 10 de <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">ejemplo de BasicHLSL10</a>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

Este es un ejemplo parcial de cómo declarar el estado de la comparación de muestra y llamar a una muestra de comparación en Direct3D 10.


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

