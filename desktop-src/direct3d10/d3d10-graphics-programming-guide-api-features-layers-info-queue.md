---
description: Personalizar la salida de depuración con ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalizar la salida de depuración con ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080230"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Personalizar la salida de depuración con ID3D10InfoQueue (Direct3D 10)

La cola de información se administra mediante una interfaz (vea la [**interfaz ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) que almacena, recupera y filtra los mensajes de depuración. La cola consta de: una cola de mensajes, una pila de filtros de almacenamiento opcional y una pila de filtros de recuperación opcional. La pila de filtros de almacenamiento se puede usar para filtrar los mensajes que desea almacenar; la pila de filtros de recuperación se puede usar para filtrar los mensajes que desea almacenar. Una vez que haya filtrado un mensaje, el mensaje se imprimirá en la ventana de depuración y se almacenará en la pila adecuada.

En general:

-   Llamar a [**ID3D10InfoQueue:: AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) para generar mensajes definidos por el usuario
-   La llamada a [**ID3D10InfoQueue:: GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) se usa para obtener mensajes (que pasan un filtro de recuperación opcional).

## <a name="registry-controls"></a>Controles del registro

Use las claves del registro para ajustar la configuración del filtro, ajustar los puntos de interrupción y silenciar los resultados de la depuración. El nivel de depuración comprobará estas rutas de acceso para las claves del registro; se usará la primera ruta de acceso encontrada.

1.  HKCU \\ software \\ Microsoft \\ Direct3D \\<subclave definida por el usuario>
2.  HKLM \\ software \\ Microsoft \\ Direct3D \\<subclave definida por el usuario>
3.  HKCU \\ software \\ Microsoft \\ Direct3D

Donde:

-   El usuario actual de la versión HKEY es el de la \_ \_ \_ máquina local \_ .
-   <subclave definida por el usuario> es un nombre arbitrario para almacenar la configuración de depuración de una aplicación

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtrado de mensajes de depuración con claves del registro

Si el registro contiene una clave InfoQueueStorageFilterOverride (y es distinto de cero), se pueden filtrar los mensajes (y la salida de depuración) agregando los siguientes controles del registro.

-   DWORD silenciar \_ categoría \_ \* : salida de depuración si esta clave es distinta de cero.
-   \_Gravedad de silencio \_ \* de DWORD: la salida de depuración está deshabilitada si esta clave es distinta de cero.
-   Identificador de \_ silencio \_ \* de DWORD: el nombre o número del mensaje se puede usar para \* (al igual que para el ID. de interrupción \_ \_ \* descrito anteriormente). La salida de depuración está deshabilitada si esta clave es distinta de cero.
-   DWORD Unmute \_ Severity \_ info: la salida de depuración está habilitada si esta clave es distinta de cero. De forma predeterminada, cuando InfoQueueStorageFilterOverride está habilitado, los mensajes de depuración con información de gravedad están silenciados; por lo tanto, esta clave permite volver a activar la información.

Estos controles cambian si se registra o muestra un mensaje; no afectan a si una API supera o no.

### <a name="setting-break-conditions-using-registry-keys"></a>Establecer condiciones de interrupción mediante claves del registro

Las aplicaciones pueden verse obligadas a interrumpir en un mensaje con las siguientes claves del registro.

**EnableBreakOnMessage** : esta clave permite la interrupción de mensajes (y hace que se omita la configuración de SetBreakOnCategory ()/SetBreakOnSeverity ()/SetBreakOnID (). Los mensajes reales en los que se debe interrumpir se definen mediante uno o varios valores de breakon \_ \* definidos a continuación.

-   **\_ Breakon \_Categoría \** _-break en cualquier mensaje que pase a través de los filtros de almacenamiento. \_ es uno de los mensajes de la \_ categoría de mensajes D3D10 \_ .
-   **\_ Breakon \_Gravedad \** _-break en cualquier mensaje que pase a través de los filtros de almacenamiento. \_ es uno de los mensajes de gravedad del mensaje de D3D10 \_ \_ \_ .
-   **\_ Breakon \_Identificador \** _-break en cualquier mensaje que pase a través de los filtros de almacenamiento. \_ es uno de los \_ mensajes de \_ ID. de mensaje D3D10 \_ o puede ser el valor numérico de la enumeración error. Por ejemplo, supongamos que el mensaje con el identificador "D3D10 \_ Message \_ ID \_ hipotético" tenía el valor 123 en la \_ \_ enumeración D3D10 Message ID. En este caso, la creación del valor de \_ ID. de interrupción \_ hipotética = 1 o el \_ ID. de interrupción \_ 123 = 1 realizaría la misma interrupción cuando se encuentra un mensaje con el ID. de mensaje de identificador D3D10 \_ \_ \_ hipotética.

### <a name="muting-debug-output-using-registry-keys"></a>Silenciar la salida de depuración con claves del registro

La salida de depuración se puede silenciar mediante una clave MuteDebugOutput. La presencia de este valor en el registro fuerza la invalidación del método [**ID3D10InfoQueue:: SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) de InfoQueue. MuteDebugOutput detiene los mensajes que pasan el filtro de almacenamiento para que no se envíen a la salida de depuración.

## <a name="disabling-debug-layer-messages"></a>Deshabilitar mensajes de la capa de depuración

Los mensajes de la capa de depuración se pueden deshabilitar individualmente o como un grupo en tiempo de ejecución mediante la especificación de filtros mediante [**ID3D10InfoQueue:: AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries). El argumento *pFilter* de **ID3D10InfoQueue:: AddStorageFilterEntries** toma una estructura de filtro de [**cola de D3D10 \_ \_ \_ info**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) que contiene una lista de permitidos y una lista de denegación. Las listas de permitidos y denegadas se describen en [**D3D10 \_ info \_ Queue \_ Filter \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) Structures que permiten que los filtros se especifiquen mediante categoría, Severity y el ID. de mensaje individual.

El código siguiente es un ejemplo de la configuración de la [**interfaz ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) para denegar el \_ mensaje D3D10 Message \_ ID \_ Device \_ Draw \_ \_ búfer \_ demasiado \_ pequeño.


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Niveles de API](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[Características de la API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



