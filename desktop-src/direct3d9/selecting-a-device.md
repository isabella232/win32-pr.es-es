---
description: Las aplicaciones pueden consultar hardware para detectar los tipos de dispositivos Direct3D admitidos. Esta sección contiene información sobre las tareas principales implicadas en la enumeración de adaptadores de pantalla y la selección de dispositivos Direct3D.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Selección de un dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63428e15948e15790364f310d55989a9bbc7339846f7db5d301e316bee4d872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044253"
---
# <a name="selecting-a-device-direct3d-9"></a>Selección de un dispositivo (Direct3D 9)

Las aplicaciones pueden consultar hardware para detectar los tipos de dispositivos Direct3D admitidos. Esta sección contiene información sobre las tareas principales implicadas en la enumeración de adaptadores de pantalla y la selección de dispositivos Direct3D.

Una aplicación debe realizar una serie de tareas para seleccionar un dispositivo Direct3D adecuado. Tenga en cuenta que los pasos siguientes están pensados para una aplicación de pantalla completa y que, en la mayoría de los casos, una aplicación con ventanas puede omitir la mayoría de estos pasos.

1.  Inicialmente, la aplicación debe enumerar los adaptadores de pantalla del sistema. Un adaptador es un fragmento físico de hardware. Tenga en cuenta que la tarjeta gráfica puede contener más de un único adaptador, como es el caso de una pantalla de dos cabezas. Las aplicaciones que no se refieren a la compatibilidad con varios monitores pueden pasar por alto este paso y pasar D3DADAPTER DEFAULT al método \_ [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) en el paso 2.
2.  Para cada adaptador, la aplicación enumera los modos de presentación admitidos mediante una llamada a [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).
3.  Si es necesario, la aplicación comprueba la presencia de aceleración de hardware en cada modo de presentación enumerado mediante una llamada a [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), como se muestra en el ejemplo de código siguiente. Tenga en cuenta que este es solo uno de los usos posibles de **IDirect3D9::CheckDeviceType**; Para obtener más información, vea [Determinar la compatibilidad con hardware (Direct3D 9).](determining-hardware-support.md)
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

    

4.  La aplicación comprueba el nivel deseado de funcionalidad para el dispositivo en este adaptador mediante una llamada al [**método IDirect3D9::GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) Se garantiza que la funcionalidad devuelta por este método es constante para un dispositivo en todos los modos de visualización, comprobados por [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).
5.  Los dispositivos siempre se pueden representar en superficies con el formato de un modo de visualización enumerado compatible con el dispositivo. Si se requiere que la aplicación se represente en una superficie de un formato diferente, puede llamar a [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat). Si el dispositivo se puede representar al formato , se garantiza que todas las funcionalidades devueltas por [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) son aplicables.
6.  Por último, la aplicación puede determinar si se admiten técnicas de multimuestreo, como el suavizado de contorno de escena completa, para un formato de representación mediante el método [**IDirect3D9::CheckDeviceMultiSampleType.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)

Después de completar los pasos anteriores, la aplicación debe tener una lista de modos de presentación en los que pueda funcionar. El último paso consiste en comprobar que hay suficiente memoria accesible para el dispositivo para dar cabida al número necesario de búferes y suavizado de contorno. Esta prueba es necesaria porque el consumo de memoria para el modo y la combinación de varios muestreos es imposible de predecir sin comprobarlo. Además, es posible que algunas arquitecturas de adaptadores de pantalla no tengan una cantidad constante de memoria accesible para dispositivos. Esto significa que una aplicación debe ser capaz de notificar errores de memoria de vídeo fuera de vídeo al pasar al modo de pantalla completa. Normalmente, una aplicación debe quitar el modo de pantalla completa de la lista de modos que ofrece a un usuario, o bien debe intentar consumir menos memoria reduciendo el número de búferes de reserva o mediante una técnica de multimuestreo menos compleja.

Una aplicación en ventanas realiza un conjunto similar de tareas.

1.  Determina el rectángulo de escritorio cubierto por el área cliente de la ventana.
2.  Enumera los adaptadores, buscando el adaptador cuyo monitor cubre el área de cliente. Si el área de cliente es propiedad de más de un adaptador, la aplicación puede optar por dirigir cada adaptador de forma independiente, o bien para dirigir un único adaptador y tener píxeles de transferencia de Direct3D de un dispositivo a otro en la presentación. La aplicación también puede pasar por alto los dos pasos anteriores y usar el adaptador D3DADAPTER \_ DEFAULT. Tenga en cuenta que esto podría dar lugar a una operación más lenta cuando la ventana se coloca en un monitor secundario.
3.  La aplicación debe llamar a [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) para determinar si el dispositivo puede admitir la representación en un búfer de reserva del formato especificado en modo de escritorio. [**IDirect3D9::GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) se puede usar para determinar el formato de presentación del escritorio, como se muestra en el ejemplo de código siguiente.
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

 

 
