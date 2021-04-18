---
title: Nuevos tipos de recursos
description: Se han agregado varios tipos de recursos nuevos en Direct3D 11.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Búfer de direcciones de byte (Introducción)
- Búfer de lectura/escritura (Introducción)
- Búfer estructurado (información general)
- Búfer de acceso desordenado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421049"
---
# <a name="new-resource-types"></a>Nuevos tipos de recursos

Se han agregado varios tipos de recursos nuevos en Direct3D 11.

-   [Búferes y texturas de lectura/escritura](#readwrite-buffers-and-textures)
-   [Búfer estructurado](#structured-buffer)
-   [Búfer de direcciones de bytes](#byte-address-buffer)
-   [Búfer o textura de acceso desordenado](#unordered-access-buffer-or-texture)
    -   [Anexar y consumir búfer](#append-and-consume-buffer)
-   [Temas relacionados](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Búferes y texturas de lectura/escritura

Los recursos del modelo de sombreador 4 son de solo lectura. El modelo de sombreador 5 implementa un nuevo conjunto correspondiente de recursos de lectura y escritura:

-   [RWBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Estos recursos requieren una variable de recurso para tener acceso a la memoria (a través de la indización), ya que no hay ningún método para tener acceso a la memoria directamente. Se puede utilizar una variable de recurso en los lados izquierdo y derecho de una ecuación; Si se utiliza en el lado derecho, el tipo de plantilla debe ser un único componente (float, int o uint).

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



Use esta estructura para declarar un búfer estructurado como el siguiente:


```
StructuredBuffer<MyStruct> mySB;
```



Además de la indización, un búfer estructurado admite el acceso a un solo miembro como este:


```
float4 myColor = mySb[27].Color;
```



Use los siguientes tipos de objeto para tener acceso a un búfer estructurado:

-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) es un búfer estructurado de solo lectura.
-   [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) es un búfer estructurado de lectura/escritura.

[Las funciones atómicas](direct3d-11-advanced-stages-cs-atomic-functions.md) que implementan operaciones de interbloqueos se permiten en los elementos int y uint de un **RWStructuredBuffer**.

## <a name="byte-address-buffer"></a>Búfer de direcciones de bytes

Un búfer de direcciones de bytes es un búfer cuyo contenido es direccionable por un desplazamiento de bytes. Normalmente, el contenido de un [búfer](overviews-direct3d-11-resources-buffers-intro.md) se indexa por elemento mediante un intervalo para cada elemento (s) y el número de elemento (N) según lo especificado por S \* N. Un búfer de direcciones de bytes, que también se puede llamar búfer sin formato, utiliza un desplazamiento de valor de bytes desde el principio del búfer para obtener acceso a los datos. El valor de byte debe ser un múltiplo de cuatro para que esté alineado con DWORD. Si se proporciona cualquier otro valor, el comportamiento es indefinido.

El modelo de sombreador 5 presenta objetos para obtener acceso a un [búfer de direcciones de bytes de solo lectura](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) , así como a un [búfer de direcciones de bytes de lectura y escritura](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer). El contenido de un búfer de direcciones de bytes está diseñado para ser un entero sin signo de 32 bits. Si el valor del búfer no es realmente un entero sin signo, use una función como [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) para leerlo.

## <a name="unordered-access-buffer-or-texture"></a>Búfer o textura de acceso desordenado

Un recurso de acceso desordenado (que incluye búferes, texturas y matrices de texturas, sin muestreo múltiple), permite el acceso de lectura y escritura desordenado temporal desde varios subprocesos. Esto significa que varios subprocesos pueden leer o escribir simultáneamente este tipo de recurso sin generar conflictos de memoria a través del uso de [funciones atómicas](direct3d-11-advanced-stages-cs-atomic-functions.md).

Cree un búfer de acceso desordenado o una textura llamando a una función como [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) o [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) y pasando la marca **de \_ \_ \_ acceso desordenado de D3D11 enlace** desde la enumeración de [**\_ \_ marca de enlace D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .

Los recursos de acceso desordenados solo se pueden enlazar a los sombreadores de píxeles y los sombreadores de cálculo. Durante la ejecución, los sombreadores de píxeles o los sombreadores de cálculo que se ejecutan en paralelo tienen los mismos recursos de acceso desordenados enlazados.

### <a name="append-and-consume-buffer"></a>Anexar y consumir búfer

Un búfer Append y consume es un tipo especial de recurso no ordenado que permite agregar y quitar valores del final de un búfer de forma similar a como funciona una pila.

Un búfer de anexión y consumo debe ser un búfer estructurado:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Usar estos recursos a través de sus métodos, estos recursos no usan variables de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general del sombreador de cálculo](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 