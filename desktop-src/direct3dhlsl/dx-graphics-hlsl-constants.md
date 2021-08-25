---
title: Constantes de sombreador (HLSL)
description: En El modelo de sombreador 4, las constantes del sombreador se almacenan en uno o varios recursos de búfer en memoria.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- búfer constante
- búfer de textura
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a6b2ffa9168e870aeb405badb6ff71b0a4a59b23d76947e56a9c085ed0107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726555"
---
# <a name="shader-constants-hlsl"></a>Constantes de sombreador (HLSL)

En El modelo de sombreador 4, las constantes del sombreador se almacenan en uno o varios recursos de búfer en memoria. Se pueden organizar en dos tipos de búferes: búferes constantes (cbuffers) y búferes de textura (tbuffers). Los búferes constantes están optimizados para el uso de variables constantes, lo que se caracteriza por un acceso de menor latencia y una actualización más frecuente desde la CPU. Por este motivo, se aplican restricciones de tamaño, diseño y acceso adicionales a estos recursos. Se accede a los búferes de textura como texturas y tienen un mejor rendimiento para los datos indexados arbitrariamente. Independientemente del tipo de recurso que use, no hay ningún límite en el número de búferes constantes o búferes de textura que una aplicación puede crear.

Declarar un búfer constante o un búfer de textura es muy similar a una declaración de estructura en C, con la adición de las palabras clave **register** y **packoffset** para asignar manualmente registros o empaquetar datos.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[ *Nombre* \] \[: **register**(b \# ) { \] *VariableDeclaration* \[ : **packoffset**(c \# .xyzw) \] ;      ... }; |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[en \] El tipo de búfer.



| BufferType | Descripción     |
|------------|-----------------|
| cbuffer    | búfer constante |
| tbuffer    | búfer de textura  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

\[en \] Opcional, cadena ASCII que contiene un nombre de búfer único.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b \# )
</dt> <dd>

\[en \] la palabra clave Optional, se usa para empaquetar manualmente los datos constantes. Las constantes se pueden empaquetar en un registro solo en un búfer constante, donde el registro inicial lo da el número de registro ( *\#* ).

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[en \] Declaración de variable, similar a una declaración de miembro de estructura. Puede ser cualquier tipo HLSL o objeto de efecto (excepto una textura o un objeto sampler).

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# .xyzw)
</dt> <dd>

\[en \] la palabra clave Optional, se usa para empaquetar manualmente los datos constantes. Las constantes se pueden empaquetar en cualquier búfer constante, donde el número de registro lo da ( *\#* ). El empaquetado de sub-componente (mediante el desdobado xyzw) está disponible para las constantes cuyo tamaño cabe dentro de un único registro (no cruza un límite de registro). Por ejemplo, un elemento float4 no se pudo empaquetar en un único registro a partir del componente y porque no cabría en un registro de cuatro componentes.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los búferes constantes reducen el ancho de banda necesario para actualizar las constantes del sombreador, ya que permiten agrupar y confirmar constantes de sombreador al mismo tiempo en lugar de realizar llamadas individuales para confirmar cada constante por separado.

Un búfer constante es un recurso de búfer especializado al que se accede como un búfer. Cada búfer constante puede contener hasta 4096 [vectores](dx-graphics-hlsl-vector.md); cada vector contiene hasta cuatro valores de 32 bits. Puede enlazar hasta 14 búferes constantes por fase de canalización (2 ranuras adicionales están reservadas para uso interno).

Un búfer de textura es un recurso de búfer especializado al que se accede como una textura. El acceso de textura (en comparación con el acceso al búfer) puede tener un mejor rendimiento para los datos indexados arbitrariamente. Puede enlazar hasta 128 búferes de textura por fase de canalización.

Un recurso de búfer está diseñado para minimizar la sobrecarga de establecer constantes de sombreador. El marco de efectos (consulte La interfaz [**ID3D10Effect)**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)administrará la actualización de búferes de constantes y texturas, o bien puede usar la API de Direct3D para actualizar los búferes (consulte Copiar y acceder a los datos de recursos [(Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) para obtener información). Una aplicación también puede copiar datos de otro búfer (como un destino de representación o un destino de salida de flujo) en un búfer constante.

Para obtener más información sobre el uso de búferes constantes en una aplicación D3D10, vea Tipos de recursos [(Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) y Creación de recursos de [búfer (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)

Para obtener más información sobre el uso de búferes constantes en una aplicación D3D11, vea Introducción a los búferes en [Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) y Cómo: Crear un búfer [constante.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)

Un búfer constante no requiere que [una vista](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) esté enlazada a la canalización. Sin embargo, un búfer de textura requiere una vista y debe enlazarse a una ranura de textura (o debe enlazarse con [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) cuando se usa un efecto).

Hay dos maneras de empaquetar datos de constantes: mediante las palabras clave [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) y [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

Diferencias entre Direct3D 9 y Direct3D 10 y 11:

- A diferencia de la asignación automática de constantes en Direct3D 9, que no realizaba el empaquetado y, en su lugar, asignaba cada variable a un conjunto de registros float4, las variables constantes HLSL siguen las reglas de empaquetado en Direct3D 10 y 11.



 

### <a name="organizing-constant-buffers"></a>Organización de búferes constantes

Los búferes constantes reducen el ancho de banda necesario para actualizar las constantes del sombreador, ya que permiten agrupar y confirmar constantes de sombreador al mismo tiempo en lugar de realizar llamadas individuales para confirmar cada constante por separado.

La mejor forma de usar búferes de constantes con eficiencia es organizar las variables de sombreador en búferes de constantes según su frecuencia de actualización. Esto permite que una aplicación minimice el ancho de banda necesario para actualizar las constantes del sombreador. Por ejemplo, un sombreador podría declarar dos búferes constantes y organizar los datos de cada uno en función de su frecuencia de actualización: los datos que deben actualizarse por objeto (como una matriz mundial) se agrupan en un búfer constante que se puede actualizar para cada objeto. Esto es independiente de los datos que caracteriza una escena y, por lo tanto, es probable que se actualice con mucha menos frecuencia (cuando cambia la escena).


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a>Búferes de constantes predeterminados

Hay dos búferes de constantes predeterminados disponibles, $Global y $Param. Las variables que se colocan en el ámbito global se agregan implícitamente al $Global cbuffer, mediante el mismo método de empaquetado que se usa para los cbuffers. Los parámetros uniformes de la lista de parámetros de una función aparecen en $Param búfer constante cuando se compila un sombreador fuera del marco de efectos. Cuando se compilan dentro del marco de efectos, todos los uniformes deben resolverse en variables definidas en el ámbito global.

## <a name="examples"></a>Ejemplos

Este es un ejemplo de [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) que es un búfer de textura que se forma con una matriz de matrices.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



En esta declaración de ejemplo se asigna manualmente un búfer constante para iniciarse en un registro determinado y también se empaquetan elementos concretos por subcomponentes.


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

