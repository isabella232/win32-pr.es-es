---
title: Tipo de sampler
description: Use la sintaxis siguiente para declarar el estado del sampler, así como el estado de comparación del muestreador.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Tipo de sampler HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237880ab84bedc1671fdbf0eaa87e08ad0ba85ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880611"
---
# <a name="sampler-type"></a>Tipo de sampler

Use la sintaxis siguiente para declarar el estado del sampler, así como el estado de comparación del muestreador.



<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10 y versiones posteriores:<br/> Esta es la sintaxis de un sampler en Direct3D 9.<br/> 
<table>
<tbody>
<tr class="odd">
<td>sampler <em>Name</em>  =  <em>SamplerType</em>{ Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La sintaxis de un muestreador en Direct3D 10 y versiones posteriores cambia ligeramente para admitir objetos de textura y matrices de muestreador.</p>

<table>
<tbody>
<tr class="odd">
<td><em>SamplerType Name[Index]</em>{ [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>Sampler
</dt> <dd>

Solo Direct3D 9. Palabra clave Required.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre de la variable sampler.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Índice\]*
</dt> <dd>

Solo Direct3D 10 y versiones posteriores. Tamaño opcional de la matriz; entero positivo mayor o igual que 1.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*
</dt> <dd>

\[en el tipo sampler, que es uno de los \] siguientes: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler \_ state*, *SamplerState*.

Diferencias entre Direct3D 9 y Direct3D 10 y versiones posteriores:

- Direct3D 10 y versiones posteriores admiten un tipo de sampler adicional: *SamplerComparisonState.*



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Textura* = <*variable de \_ textura>;*
</dt> <dd>

Solo Direct3D 9. Variable de textura. La *palabra clave Texture* es necesaria en el lado izquierdo; el nombre de la variable pertenece al lado derecho de la expresión entre corchetes angulares.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state \_ name = state \_ value*
</dt> <dd>

\[en \] Asignaciones de estado opcionales. El lado izquierdo de una asignación es un nombre de estado, el lado derecho es el valor de estado. Todas las asignaciones de estado deben aparecer dentro de un bloque de instrucciones (entre llaves). Cada instrucción se separa con un punto y coma. En la tabla siguiente se enumeran los posibles nombres de estado.


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



El lado derecho de cada expresión es el valor asignado a cada estado. Consulte la [**estructura D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) para ver los valores de estado posibles para Direct3D 11. Hay una relación de 1 a 1 entre los nombres de estado y los miembros de la estructura . Consulte el ejemplo siguiente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al implementar un efecto, el estado del muestreador es uno de varios tipos de estado que es posible que tenga que configurar en la canalización para la representación. Para obtener una lista de todos los estados posibles que puede establecer en un efecto, vea:

-   Direct3D 10 usa grupos [de estados](/windows/desktop/direct3d10/d3d10-effect-states).
-   Direct3D 9 usa estados [individuales.](/windows/desktop/direct3d9/effect-states)

## <a name="example"></a>Ejemplo



<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10:<br/> Este es un ejemplo parcial de un sampler de Direct3D 9 del <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">ejemplo BasicHLSL</a>.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = &lt;g_MeshTexture&gt;;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p>Este es un ejemplo parcial de un muestreador de Direct3D 10 del <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">ejemplo BasicHLSL10</a>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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



 

Este es un ejemplo parcial de declarar el estado de comparación del muestreador y llamar a un muestreador de comparación en Direct3D 10.


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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

