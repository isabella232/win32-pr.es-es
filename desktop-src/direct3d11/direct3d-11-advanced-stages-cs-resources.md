---
title: Nuevos tipos de recursos
description: Se han agregado varios tipos de recursos nuevos en Direct3D 11.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Búfer de direcciones de bytes (información general)
- Búfer de lectura y escritura (información general)
- Búfer estructurado (información general)
- Búfer de acceso desordenado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465405"
---
# <a name="new-resource-types"></a>Nuevos tipos de recursos

Se han agregado varios tipos de recursos nuevos en Direct3D 11.

-   [Búferes y texturas de lectura y escritura](#readwrite-buffers-and-textures)
-   [Búfer estructurado](#structured-buffer)
-   [Búfer de direcciones de bytes](#byte-address-buffer)
-   [Búfer o textura de acceso desordenado](#unordered-access-buffer-or-texture)
    -   [Anexar y consumir búfer](#append-and-consume-buffer)
-   [Temas relacionados](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Búferes y texturas de lectura y escritura

Los recursos del modelo 4 del sombreador son de solo lectura. El modelo de sombreador 5 implementa un nuevo conjunto correspondiente de recursos de lectura y escritura:

-   [RWBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Estos recursos requieren una variable de recurso para acceder a la memoria (a través de la indexación), ya que no hay ningún método para acceder directamente a la memoria. Se puede usar una variable de recurso en los lados izquierdo y derecho de una ecuación; si se usa en el lado derecho, el tipo de plantilla debe ser un solo componente (float, int o uint).

## <a name="structured-buffer"></a>Búfer estructurado

Un búfer estructurado es un búfer que contiene elementos de igual tamaño. Use una estructura con uno o varios tipos de miembro para definir un elemento. Esta es una estructura con tres miembros.


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



Use esta estructura para declarar un búfer estructurado como este:


```
StructuredBuffer<MyStruct> mySB;
```



Además de la indexación, un búfer estructurado admite el acceso a un único miembro como el siguiente:


```
float4 myColor = mySb[27].Color;
```



Use los siguientes tipos de objeto para acceder a un búfer estructurado:

-   [StructuredBuffer es](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) un búfer estructurado de solo lectura.
-   [RWStructuredBuffer es](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) un búfer estructurado de lectura/escritura.

[Las funciones atómicas](direct3d-11-advanced-stages-cs-atomic-functions.md) que implementan operaciones entrelazados se permiten en los elementos int y uint de **rwStructuredBuffer.**

## <a name="byte-address-buffer"></a>Búfer de direcciones de bytes

Un búfer de direcciones de bytes es un búfer cuyo contenido se puede direccionar mediante un desplazamiento de bytes. Normalmente, el contenido [](overviews-direct3d-11-resources-buffers-intro.md) de un búfer se indexa por elemento mediante un paso para cada elemento (S) y el número de elemento (N) tal como lo especifica S \* N. Un búfer de direcciones de bytes, que también se puede denominar búfer sin procesar, usa un desplazamiento de valor de byte desde el principio del búfer para acceder a los datos. El valor de byte debe ser un múltiplo de cuatro para que esté alineado con DWORD. Si se proporciona cualquier otro valor, el comportamiento es indefinido.

El modelo de sombreador 5 presenta objetos para tener acceso a un búfer de direcciones [de bytes](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) de solo lectura, así como a un búfer [de direcciones de bytes de lectura y escritura.](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) El contenido de un búfer de direcciones de bytes está diseñado para ser un entero de 32 bits sin signo; Si el valor del búfer no es realmente un entero sin signo, use una función como [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) para leerlo.

## <a name="unordered-access-buffer-or-texture"></a>Búfer o textura de acceso desordenado

Un recurso de acceso desordenado (que incluye búferes, texturas y matrices de texturas, sin multimuestreo), permite el acceso de lectura y escritura sin ordenar temporalmente desde varios subprocesos. Esto significa que varios subprocesos pueden leer o escribir simultáneamente este tipo de recurso sin generar conflictos de memoria mediante el uso de [Funciones atómicas](direct3d-11-advanced-stages-cs-atomic-functions.md).

Cree un búfer de acceso no ordenado o una textura llamando a una función como [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) o [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) y pasando la marca DE ACCESO **\_ \_ UNORDERED \_ BIND D3D11** de la enumeración BIND FLAG de [**\_ \_ D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)

Los recursos de acceso desordenado solo se pueden enlazar a sombreadores de píxeles y sombreadores de proceso. Durante la ejecución, los sombreadores de píxeles o los sombreadores de proceso que se ejecutan en paralelo tienen enlazados los mismos recursos de acceso desordenados.

### <a name="append-and-consume-buffer"></a>Anexar y consumir búfer

Un búfer anexar y consumir es un tipo especial de un recurso desordenado que admite la adición y eliminación de valores del final de un búfer de forma similar a la forma en que funciona una pila.

Un búfer append y consume debe ser un búfer estructurado:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Use estos recursos a través de sus métodos; estos recursos no usan variables de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el sombreador de proceso](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 