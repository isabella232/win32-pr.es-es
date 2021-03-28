---
title: Clonar un efecto
description: La clonación de un efecto crea una segunda copia prácticamente idéntica del efecto.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777239"
---
# <a name="cloning-an-effect"></a>Clonar un efecto

La clonación de un efecto crea una segunda copia prácticamente idéntica del efecto. Vea el siguiente calificador único para obtener una explicación de por qué no es exacta. Una segunda copia de un efecto es útil cuando se desea usar el marco de trabajo de efectos en varios subprocesos, ya que el tiempo de ejecución del efecto no es seguro para subprocesos para mantener un alto rendimiento.

Dado que los contextos de dispositivo también son no seguros para subprocesos, los distintos subprocesos deben pasar distintos contextos de dispositivo al método ID3DX11EffectPass:: Apply.

Un efecto se puede clonar con la siguiente sintaxis:


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



En el ejemplo anterior, la copia clonada encapsulará el mismo estado que el efecto original, independientemente del estado en el que se encuentra el efecto original. En concreto:

1.  Si pEffect está optimizado, se optimiza el efecto pCloned
2.  Si pEffect tiene algunas variables administradas por el usuario, el efecto pCloned tendrá las mismas variables administradas por el usuario (vea la descripción única a continuación).
3.  Todas las actualizaciones de variables pendientes (hasta que se aplique una llamada a aplicar actualiza el estado del dispositivo) en pEffect estarán pendientes en pClonedEffect

Los siguientes objetos de dispositivo de Direct3D 11 son inmutables o nunca actualizados por el marco de trabajo de Effects, por lo que el efecto clonado apuntará a los mismos objetos que el efecto original:

1.  Objetos de bloque de estado (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Sombreadores
3.  Instancias de clase
4.  Texturas (sin incluir los búferes de textura)
5.  Vistas de acceso desordenado

Los siguientes objetos de dispositivo de Direct3D 11 son inmutables y modificados por el tiempo de ejecución del efecto (a menos que sea administrado por el usuario o único en un efecto clonado). las nuevas copias de estos objetos se crean cuando no es Single:

1.  Búferes de constantes
2.  Búferes de textura

## <a name="single-constant-buffers-and-texture-buffers"></a>Búferes de una sola constante y búferes de textura

Tenga en cuenta que este debate se aplica tanto a los búferes de constantes como a las texturas, pero se supone que los búferes de constantes se pueden leer fácilmente.

Puede haber casos en los que un búfer de constantes solo se actualice en un subproceso, pero el estado del dispositivo establecido por efectos clonados usará estos datos. Por ejemplo, el efecto principal puede actualizar el mundo y ver las matrices a las que se hace referencia desde los sombreadores en efectos clonados que no cambian el mundo y ven matrices. En estos casos, los efectos clonados deben hacer referencia al búfer de constantes actual en lugar de volver a crear uno.

Hay dos maneras de lograr este resultado deseado:

1.  Use ID3DX11EffectConstantBuffer:: SetConstantBuffer en el efecto clonado para que sea administrado por el usuario.
2.  Marcar el búfer de constantes como "único" en el código HLSL, forzando al tiempo de ejecución de efecto a tratar es como administrado por el usuario después de la clonación

Hay dos diferencias entre los dos métodos anteriores. En primer lugar, en el método 1 se creará un nuevo ID3D11Buffer y se llamará al usuario antes de SetConstantBuffer. Además, después de llamar a UndoSetConstantBuffer en el efecto clonado, la variable del método 1will apunta al búfer recién creado (que los efectos actualizarán al aplicarse) mientras que la variable del método 2 continuará señalando al búfer original (no se actualizará en la aplicación).

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



Durante la clonación, el efecto clonado creará un nuevo ID3D11Buffer para ObjectData y rellenará su contenido en Apply, pero hará referencia al ID3D11Buffer original para ViewData. El calificador único se puede pasar por alto en el proceso de clonación estableciendo la marca de la \_ fuerza de clonación del efecto de D3DX11 \_ \_ \_ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




