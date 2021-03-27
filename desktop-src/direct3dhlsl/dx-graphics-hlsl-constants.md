---
title: Constantes de sombreador (HLSL)
description: En el modelo de sombreador 4, las constantes de sombreador se almacenan en uno o varios recursos de búfer en la memoria.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- búfer de constantes
- búfer de textura
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800722"
---
# <a name="shader-constants-hlsl"></a>Constantes de sombreador (HLSL)

En el modelo de sombreador 4, las constantes de sombreador se almacenan en uno o varios recursos de búfer en la memoria. Se pueden organizar en dos tipos de búferes: búferes de constantes (cbuffers) y búferes de textura (tbuffers). Los búferes de constantes están optimizados para el uso de variables constantes, que se caracteriza por un acceso de baja latencia y una actualización más frecuente de la CPU. Por esta razón, se aplican restricciones de acceso, diseño y tamaño adicionales a estos recursos. Se tiene acceso a los búferes de texturas como las texturas y funcionan mejor para los datos indexados de forma arbitraria. Independientemente del tipo de recurso que use, no hay límite para el número de búferes de constantes o de texturas que puede crear una aplicación.

Declarar un búfer de constantes o un búfer de textura es muy similar a una declaración de estructura en C, con la adición de las palabras clave **Register** y **packoffset** para asignar manualmente los registros o empaquetar los datos.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[ *Nombre* \] de \[: **Register**(b \# ) \] { *VariableDeclaration* \[ : **packoffset**(c \# . xyzw) \] ;      ... }; |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[en \] el tipo de búfer.



| BufferType | Descripción     |
|------------|-----------------|
| cbuffer    | búfer de constantes |
| tbuffer    | búfer de textura  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

\[en \] una cadena ASCII opcional que contiene un nombre de búfer único.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**registro**(b \# )
</dt> <dd>

\[en la \] palabra clave opcional, se usa para empaquetar manualmente los datos constantes. Las constantes se pueden empaquetar en un registro solo en un búfer de constantes, donde el registro de inicio se proporciona mediante el número de registro ( *\#* ).

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[en \] la declaración de variable, similar a una declaración de miembro de estructura. Puede ser cualquier objeto de tipo HLSL o de efecto (excepto una textura o un objeto de muestra).

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . xyzw)
</dt> <dd>

\[en la \] palabra clave opcional, se usa para empaquetar manualmente los datos constantes. Las constantes se pueden empaquetar en cualquier búfer de constantes, donde () proporciona el número de registro *\#* . El empaquetado de subcomponentes (con xyzw permutación) está disponible para las constantes cuyo tamaño cabe en un solo registro (no cruce un límite de registro). Por ejemplo, una FLOAT4 no se pudo empaquetar en un solo registro a partir del componente y porque no cabe en un registro de cuatro componentes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los búferes de constantes reducen el ancho de banda necesario para actualizar las constantes de sombreador al permitir que las constantes de sombreador se agrupen y se confirmen al mismo tiempo, en lugar de realizar llamadas individuales para confirmar cada constante por separado.

Un búfer de constantes es un recurso de búfer especializado al que se tiene acceso como un búfer. Cada búfer de constantes puede contener hasta 4096 [vectores](dx-graphics-hlsl-vector.md); cada vector contiene valores de hasta 4 32 bits. Puede enlazar hasta 14 búferes de constantes por fase de canalización (2 ranuras adicionales se reservan para uso interno).

Un búfer de textura es un recurso de búfer especializado al que se tiene acceso como una textura. El acceso de textura (en comparación con el acceso al búfer) puede mejorar el rendimiento de los datos indexados de forma arbitraria. Puede enlazar hasta 128 búferes de textura por fase de canalización.

Un recurso de búfer está diseñado para minimizar la sobrecarga que supone establecer constantes de sombreador. El marco de efecto (consulte la [**interfaz ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) administrará los búferes de constante y de textura, o puede usar la API de Direct3D para actualizar los búferes (consulte [copia y acceso a los datos de recursos (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) para obtener información). Una aplicación también puede copiar datos de otro búfer (como un destino de representación o un destino de flujo de salida) en un búfer de constantes.

Para obtener más información sobre el uso de búferes de constantes en una aplicación D3D10, consulte [tipos de recursos (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) y [creación de recursos de búfer (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).

Para obtener información sobre Morel sobre el uso de búferes de constantes en una aplicación de D3D11, vea [Introducción a los búferes en Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) y [Cómo: crear un búfer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Un búfer de constantes no requiere que una [vista](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) esté enlazada a la canalización. Sin embargo, un búfer de textura requiere una vista y debe estar enlazada a una ranura de textura (o debe estar enlazada con [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) cuando se usa un efecto).

Hay dos maneras de empaquetar datos de constantes: mediante las palabras clave [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) y [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10 y 11:<br/> A diferencia de la asignación automática de constantes en Direct3D 9, que no realizaban el empaquetado y, en su lugar, asignaba cada variable a un conjunto de registros de FLOAT4, las variables de constantes de HLSL siguen las reglas de empaquetado en Direct3D 10 y 11.<br/> |



 

### <a name="organizing-constant-buffers"></a>Organizar búferes de constantes

Los búferes de constantes reducen el ancho de banda necesario para actualizar las constantes de sombreador al permitir que las constantes de sombreador se agrupen y se confirmen al mismo tiempo, en lugar de realizar llamadas individuales para confirmar cada constante por separado.

La mejor forma de usar búferes de constantes con eficiencia es organizar las variables de sombreador en búferes de constantes según su frecuencia de actualización. Esto permite a una aplicación minimizar el ancho de banda necesario para actualizar las constantes de sombreador. Por ejemplo, un sombreador podría declarar dos búferes de constantes y organizar los datos en cada uno de ellos según su frecuencia de actualización: los datos que deben actualizarse por objeto (como una matriz universal) se agrupan en un búfer de constantes que se puede actualizar para cada objeto. Esto es independiente de los datos que caracterizan una escena y, por tanto, es probable que se actualice con mucha menos frecuencia (cuando cambie la escena).


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

Hay dos búferes de constantes predeterminados disponibles, $Global y $Param. Las variables que se colocan en el ámbito global se agregan implícitamente al $Global CBuffer, mediante el mismo método de empaquetado que se usa para cbuffers. Los parámetros uniformes en la lista de parámetros de una función aparecen en el búfer de constantes de $Param cuando un sombreador se compila fuera del marco de trabajo de efectos. Cuando se compilan dentro del marco de trabajo de Effects, todos los uniformes deben resolverse en las variables definidas en el ámbito global.

## <a name="examples"></a>Ejemplos

Este es un ejemplo de ejemplo de [Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) que es un búfer de textura que se compone de una matriz de matrices.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



Esta declaración de ejemplo asigna manualmente un búfer de constantes para que se inicie en un registro determinado y también empaqueta elementos determinados por subcomponentes.


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

 

