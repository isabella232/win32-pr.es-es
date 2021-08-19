---
title: Uso de la capa de depuración para depurar aplicaciones
description: Aquí hablaremos sobre cómo habilitar la capa de depuración y algunos de los problemas que puede evitar mediante el uso de la capa de depuración.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ac5492b96c40b4395b2c501b764c646a8edbb06d3a6386a15cbb2534778d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912739"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Uso de la capa de depuración para depurar aplicaciones

Se recomienda usar la capa [de depuración](overviews-direct3d-11-devices-layers.md) para depurar las aplicaciones para asegurarse de que están limpias de errores y advertencias. La capa de depuración le ayuda a escribir código de Direct3D. Además, la productividad puede aumentar cuando se usa la capa de depuración porque puede ver inmediatamente las causas de errores de representación oscuros o incluso pantallas en negro en su origen. La capa de depuración proporciona advertencias para muchos problemas. Por ejemplo, la capa de depuración proporciona advertencias para estos problemas:

-   Se olvidó de establecer una textura, pero la leyó en el sombreador de píxeles.
-   Profundidad de salida, pero no tienen ningún estado de galería de símbolos de profundidad enlazado
-   Error al crear texturas con INVALIDARG

Aquí hablaremos sobre cómo habilitar la capa [de depuración](overviews-direct3d-11-devices-layers.md) y algunos de los problemas que puede evitar mediante el uso de la capa de depuración.

-   [Habilitación de la capa de depuración](#enabling-the-debug-layer)
-   [Evitar errores en la aplicación con la capa de depuración](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [No pasar punteros NULL a Map](#dont-pass-null-pointers-to-map)
    -   [Cuadro de origen Desenlazador dentro de los recursos de origen y destino](#confine-source-box-within-source-and-destination-resources)
    -   [No quitar DiscardResource ni DiscardView](#dont-drop-discardresource-or-discardview)
-   [Temas relacionados](#related-topics)

## <a name="enabling-the-debug-layer"></a>Habilitación de la capa de depuración

Para habilitar la capa de depuración [,](overviews-direct3d-11-devices-layers.md)especifique la marca [**D3D11 \_ CREATE DEVICE \_ \_ DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) en el parámetro *Flags* cuando llame a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear el dispositivo de representación. En este código de ejemplo se muestra cómo habilitar la capa de depuración cuando Microsoft Visual Studio proyecto está en una compilación de depuración:


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a>Evitar errores en la aplicación con la capa de depuración

Si usa incorrectamente la API de Direct3D 11 [](overviews-direct3d-11-devices-layers.md) o pasa parámetros incorrectos, la salida de depuración de la capa de depuración notifica un error o una advertencia. A continuación, puede corregir el error. A continuación, se observan algunos problemas de codificación que pueden provocar un comportamiento indefinido o incluso que el sistema operativo se bloquee. Puede detectar y evitar estos problemas mediante el uso de la capa de depuración.

### <a name="dont-pass-null-pointers-to-map"></a>No pasar punteros NULL a Map

Si pasa **NULL al** parámetro *pResource* o *pMappedResource* del método [**ID3D11DeviceContext::Map,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) el comportamiento de **Map** no está definido. Si ha creado un dispositivo que solo admite la capa [principal,](overviews-direct3d-11-devices-layers.md)los parámetros no válidos de **Map** pueden bloquear el sistema operativo. Si ha creado un dispositivo que admite la capa [de depuración](overviews-direct3d-11-devices-layers.md), la salida de depuración notifica un error en esta llamada **a Map** no válida.

### <a name="confine-source-box-within-source-and-destination-resources"></a>Cuadro de origen Desenlazador dentro de los recursos de origen y destino

En una llamada al método [**ID3D11DeviceContext::CopySubresourceRegion,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) el cuadro de origen debe estar dentro del recurso de origen. Los desplazamientos de destino (x, y y z) permiten desplazar el cuadro de origen al escribir en el recurso de destino, pero las dimensiones del cuadro de origen y los desplazamientos deben estar dentro del tamaño del recurso. Si intenta copiar fuera del recurso de destino o especifica un cuadro de origen mayor que el recurso de origen, el comportamiento de **CopySubresourceRegion** no está definido. Si creó un dispositivo que admite la capa [de](overviews-direct3d-11-devices-layers.md)depuración , la salida de depuración notifica un error en esta **llamada a CopySubresourceRegion** no válida. Los parámetros no válidos **para CopySubresourceRegion** provocan un comportamiento indefinido y pueden provocar una representación incorrecta, un recorte, ninguna copia o incluso la eliminación del dispositivo de representación.

### <a name="dont-drop-discardresource-or-discardview"></a>No quitar DiscardResource ni DiscardView

El runtime quita una llamada a [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) o [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) a menos que cree correctamente el recurso.

El recurso que se pasa a [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) debe haber sido creado mediante [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o [**D3D11 \_ USAGE \_ DYNAMIC;**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)de lo contrario, el tiempo de ejecución quita la llamada a **DiscardResource**.

El recurso que subyace a la vista que pasa a [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) debe haber creado con [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o [**D3D11 \_ USAGE \_ DYNAMIC;**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)de lo contrario, el runtime quita la llamada a **DiscardView**.

Si ha creado un dispositivo que admite la capa [de depuración](overviews-direct3d-11-devices-layers.md), la salida de depuración notifica un error con respecto a la llamada descartada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capas de software](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




