---
title: Usar la capa de depuración para depurar aplicaciones
description: Aquí hablaremos sobre cómo habilitar la capa de depuración y algunos de los problemas que puede evitar mediante el uso de la capa de depuración.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773711"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Usar la capa de depuración para depurar aplicaciones

Se recomienda usar la capa de [depuración](overviews-direct3d-11-devices-layers.md) para depurar las aplicaciones con el fin de asegurarse de que están limpias de errores y advertencias. La capa de depuración le ayuda a escribir código de Direct3D. Además, la productividad puede aumentar al usar la capa de depuración, ya que puede ver inmediatamente las causas de los errores de representación ocultos o incluso las pantallas negras en su origen. El nivel de depuración proporciona advertencias para muchos problemas. Por ejemplo, la capa de depuración proporciona advertencias para estos problemas:

-   Olvidó establecer una textura pero leerla en el sombreador de píxeles
-   Profundidad de salida, pero no tiene ningún límite de estado de estarcido de profundidad
-   Error de creación de textura con INVALIDARG

Aquí hablaremos sobre cómo habilitar la [capa de depuración](overviews-direct3d-11-devices-layers.md) y algunos de los problemas que puede evitar mediante el uso de la capa de depuración.

-   [Habilitar la capa de depuración](#enabling-the-debug-layer)
-   [Evitar errores en la aplicación con la capa de depuración](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [No pasar punteros NULL a la asignación](#dont-pass-null-pointers-to-map)
    -   [Cuadro de código fuente de límites dentro de los recursos de origen y de destino](#confine-source-box-within-source-and-destination-resources)
    -   [No quite DiscardResource ni DiscardView](#dont-drop-discardresource-or-discardview)
-   [Temas relacionados](#related-topics)

## <a name="enabling-the-debug-layer"></a>Habilitar la capa de depuración

Para habilitar la [capa de depuración](overviews-direct3d-11-devices-layers.md), especifique la marca de [**\_ \_ \_ depuración crear dispositivo de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) en el parámetro *Flags* al llamar a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear el dispositivo de representación. Este código de ejemplo muestra cómo habilitar la capa de depuración cuando el proyecto de Microsoft Visual Studio está en una compilación de depuración:


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

Si se emplea el uso incorrecto de la API de Direct3D 11 o se pasan parámetros incorrectos, la salida de depuración de la [capa de depuración](overviews-direct3d-11-devices-layers.md) notifica un error o una advertencia. Después, puede corregir el error. A continuación, veremos algunos problemas de codificación que pueden provocar un comportamiento indefinido o incluso que el sistema operativo se bloquee. Puede detectar y evitar estos problemas mediante el uso de la capa de depuración.

### <a name="dont-pass-null-pointers-to-map"></a>No pasar punteros NULL a la asignación

Si pasa **null** al parámetro *PreSource* o *pMappedResource* del método [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , el comportamiento de la **asignación** es indefinido. Si creó un dispositivo que solo admite la [capa básica](overviews-direct3d-11-devices-layers.md), los parámetros no válidos para **asignar** pueden bloquear el sistema operativo. Si creó un dispositivo que admite la [capa de depuración](overviews-direct3d-11-devices-layers.md), la salida de depuración notificará un error en esta llamada de **asignación** no válida.

### <a name="confine-source-box-within-source-and-destination-resources"></a>Cuadro de código fuente de límites dentro de los recursos de origen y de destino

En una llamada al método [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) , el cuadro de código fuente debe estar dentro del recurso de origen. Los desplazamientos de destino, (x, y y z) permiten que el cuadro de origen se desplace cuando se escribe en el recurso de destino, pero las dimensiones del cuadro de código fuente y los desplazamientos deben estar dentro del tamaño del recurso. Si intenta copiar fuera del recurso de destino o especifica un cuadro de código fuente mayor que el recurso de origen, el comportamiento de **CopySubresourceRegion** es indefinido. Si creó un dispositivo que admite la [capa de depuración](overviews-direct3d-11-devices-layers.md), la salida de depuración notificará un error en esta llamada **CopySubresourceRegion** no válida. Los parámetros no válidos para **CopySubresourceRegion** causan un comportamiento indefinido y pueden dar lugar a una representación, un recorte, una copia incorrectas o incluso la eliminación del dispositivo de representación.

### <a name="dont-drop-discardresource-or-discardview"></a>No quite DiscardResource ni DiscardView

El Runtime quita una llamada a [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) o [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) a menos que cree correctamente el recurso.

El recurso que se pasa a [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) se debe haber creado con [**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o [**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). de lo contrario, el tiempo de ejecución quita la llamada a **DiscardResource**.

El recurso subyacente a la vista que se pasa a [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) se debe haber creado con [**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o [**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). de lo contrario, el tiempo de ejecución quita la llamada a **DiscardView**.

Si creó un dispositivo que admite la [capa de depuración](overviews-direct3d-11-devices-layers.md), la salida de depuración notifica un error relacionado con la llamada quitada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capas de software](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




