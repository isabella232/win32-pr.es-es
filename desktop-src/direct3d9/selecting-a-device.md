---
description: Las aplicaciones pueden consultar el hardware para detectar los tipos de dispositivo Direct3D compatibles. Esta sección contiene información acerca de las tareas principales que participan en la enumeración de adaptadores de pantalla y la selección de dispositivos Direct3D.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Seleccionar un dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdfa1faf38007f00959ac7263b4538954044688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538224"
---
# <a name="selecting-a-device-direct3d-9"></a>Seleccionar un dispositivo (Direct3D 9)

Las aplicaciones pueden consultar el hardware para detectar los tipos de dispositivo Direct3D compatibles. Esta sección contiene información acerca de las tareas principales que participan en la enumeración de adaptadores de pantalla y la selección de dispositivos Direct3D.

Una aplicación debe realizar una serie de tareas para seleccionar un dispositivo Direct3D adecuado. Tenga en cuenta que los siguientes pasos están pensados para una aplicación de pantalla completa y que, en la mayoría de los casos, una aplicación en ventana puede omitir la mayoría de estos pasos.

1.  Inicialmente, la aplicación debe enumerar los adaptadores de pantalla del sistema. Un adaptador es una parte física del hardware. Tenga en cuenta que la tarjeta gráfica puede contener más de un adaptador, como es el caso de una pantalla con doble punta. Las aplicaciones que no están preocupadas por la compatibilidad con varios monitores pueden descartar este paso y pasar \_ el valor predeterminado de D3DADAPTER al método [**IDirect3D9:: EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) en el paso 2.
2.  Para cada adaptador, la aplicación enumera los modos de presentación admitidos mediante una llamada a [**IDirect3D9:: EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).
3.  Si es necesario, la aplicación comprueba la presencia de la aceleración de hardware en cada modo de presentación enumerado llamando a [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), como se muestra en el ejemplo de código siguiente. Tenga en cuenta que este es solo uno de los usos posibles de **IDirect3D9:: CheckDeviceType**; para obtener más información, vea [determinar la compatibilidad de hardware (Direct3D 9)](determining-hardware-support.md).
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  La aplicación comprueba el nivel de funcionalidad deseado para el dispositivo en este adaptador llamando al método [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) . Se garantiza que la capacidad devuelta por este método es constante para un dispositivo en todos los modos de presentación, comprobada por [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).
5.  Los dispositivos siempre pueden representar en las superficies del formato de un modo de presentación enumerado compatible con el dispositivo. Si se requiere que la aplicación se represente en una superficie de un formato diferente, puede llamar a [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat). Si el dispositivo se puede representar en el formato, se garantiza que todas las funcionalidades devueltas por [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) son aplicables.
6.  Por último, la aplicación puede determinar si se admiten técnicas de muestreo múltiple, como el suavizado de contorno completo, para un formato de representación mediante el método [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) .

Después de completar los pasos anteriores, la aplicación debe tener una lista de modos de presentación en los que pueda funcionar. El paso final consiste en comprobar que hay suficiente memoria accesible para el dispositivo disponible para dar cabida al número necesario de búferes y antialias. Esta prueba es necesaria porque el consumo de memoria para la combinación de modo y Multimuestra es imposible de predecir sin comprobarla. Además, es posible que algunas arquitecturas de adaptador de pantalla no tengan una cantidad constante de memoria accesible para dispositivos. Esto significa que una aplicación debe ser capaz de notificar errores de memoria insuficiente al entrar en el modo de pantalla completa. Normalmente, una aplicación debe quitar el modo de pantalla completa de la lista de modos que ofrece a un usuario o debe intentar consumir menos memoria reduciendo el número de búferes de reserva o usando una técnica de muestreo múltiple menos compleja.

Una aplicación en ventana realiza un conjunto similar de tareas.

1.  Determina el rectángulo del escritorio que se incluye en el área cliente de la ventana.
2.  Enumera los adaptadores, buscando el adaptador cuyo monitor cubre el área cliente. Si el área de cliente es propiedad de más de un adaptador, la aplicación puede optar por controlar cada adaptador de forma independiente, o bien controlar un adaptador único y hacer que Direct3D transfiera píxeles de un dispositivo a otro en la presentación. La aplicación también puede pasar por alto dos pasos anteriores y usar el \_ adaptador predeterminado D3DADAPTER. Tenga en cuenta que esto puede dar lugar a una operación más lenta cuando la ventana se coloca en un monitor secundario.
3.  La aplicación debe llamar a [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) para determinar si el dispositivo puede admitir la representación en un búfer de reserva del formato especificado en modo de escritorio. [**IDirect3D9:: GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) se puede usar para determinar el formato de presentación del escritorio, tal y como se muestra en el ejemplo de código siguiente.
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
