---
title: Clonación de un efecto
description: La clonación de un efecto crea una segunda copia casi idéntica del efecto.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195b4e9a42e595558acc4c512f8662c11b2acde7873e123b242ee272eeea7e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538009"
---
# <a name="cloning-an-effect"></a>Clonación de un efecto

La clonación de un efecto crea una segunda copia casi idéntica del efecto. Vea el siguiente calificador único para obtener una explicación de por qué no es exacto. Una segunda copia de un efecto es útil cuando se desea usar el marco de efectos en varios subprocesos, ya que el tiempo de ejecución del efecto no es seguro para subprocesos para mantener un alto rendimiento.

Puesto que los contextos de dispositivo también no son seguros para subprocesos, los subprocesos diferentes deben pasar contextos de dispositivo diferentes al método ID3DX11EffectPass::Apply.

Un efecto se puede clonar con la sintaxis siguiente:


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



En el ejemplo anterior, la copia clonada encapsulará el mismo estado que el efecto original, independientemente del estado en el que se encuentra el efecto original. En concreto:

1.  Si pEffect está optimizado, se optimiza pCloned Effect.
2.  Si pEffect tiene algunas variables administradas por el usuario, pCloned Effect tendrá las mismas variables administradas por el usuario (consulte la descripción única a continuación).
3.  Las actualizaciones de variables pendientes (hasta que una llamada a Apply actualice el estado del dispositivo) en pEffect estarán pendientes en pClonedEffect.

Los siguientes objetos de dispositivo Direct3D 11 son inmutables o nunca actualizados por el marco de efectos, por lo que el efecto clonado apuntará a los mismos objetos que el efecto original:

1.  Objetos de bloque de estado (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Sombreadores
3.  Instancias de clase
4.  Texturas (sin incluir búferes de textura)
5.  Vistas de acceso no ordenado

Los siguientes objetos de dispositivo Direct3D 11 son inmutables y modificados por el tiempo de ejecución del efecto (a menos que sea administrado por el usuario o único en un efecto clonado); Se crean nuevas copias de estos objetos cuando no son únicas:

1.  Búferes constantes
2.  Búferes de textura

## <a name="single-constant-buffers-and-texture-buffers"></a>Búferes constantes únicos y búferes de textura

Tenga en cuenta que esta explicación se aplica tanto a los búferes constantes como a las texturas, pero los búferes constantes se asumen para facilitar la lectura.

Puede haber casos en los que un búfer constante solo se actualice mediante un subproceso, pero el estado del dispositivo establecido por los efectos clonados usará estos datos. Por ejemplo, el efecto principal puede actualizar el mundo y ver matrices a las que se hace referencia desde sombreadores en efectos clonados que no cambian el mundo y ven matrices. En estos casos, los efectos clonados deben hacer referencia al búfer constante actual en lugar de volver a crear uno.

Hay dos maneras de lograr este resultado deseado:

1.  Use ID3DX11EffectConstantBuffer::SetConstantBuffer en el efecto clonado para que sea administrado por el usuario.
2.  Marque el búfer constante como "único" en el código HLSL, lo que obliga al tiempo de ejecución del efecto a tratarse como administrado por el usuario después de la clonación.

Hay dos diferencias entre los dos métodos anteriores. En primer lugar, en el método 1, se creará un nuevo ID3D11Buffer y se creará un usuario antes de llamar a SetConstantBuffer. Además, después de llamar a UndoSetConstantBuffer en el efecto clonado, la variable del método 1 apuntará al búfer recién creado (cuyos efectos se actualizarán en Aplicar), mientras que la variable del método 2 seguirá apuntando al búfer original (no a actualizarlo en Aplicar).

Vea el ejemplo siguiente en HLSL:


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



Durante la clonación, el efecto clonado creará un nuevo ID3D11Buffer para ObjectData y rellenará su contenido en Aplicar, pero hará referencia al ID3D11Buffer original para ViewData. El calificador único se puede omitir en el proceso de clonación estableciendo la marca D3DX11 \_ EFFECT \_ CLONE FORCE \_ \_ NONSINGLE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




