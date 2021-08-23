---
description: Personalización de la salida de depuración con ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalización de la salida de depuración con ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212b78352ccc9139c069ca5d388993fd83aca6833d77547a91401bc40380fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753835"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Personalización de la salida de depuración con ID3D10InfoQueue (Direct3D 10)

La cola de información se administra mediante una interfaz (vea [**Id3D10InfoQueue Interface)**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)que almacena, recupera y filtra los mensajes de depuración. La cola consta de: una cola de mensajes, una pila de filtros de almacenamiento opcional y una pila de filtros de recuperación opcional. La pila de filtros de almacenamiento se puede usar para filtrar los mensajes que desea almacenar; la pila de filtro de recuperación se puede usar para filtrar los mensajes que desea almacenar. Una vez filtrado un mensaje, el mensaje se imprimirá en la ventana de depuración y se almacenará en la pila adecuada.

En general:

-   Llame [**a ID3D10InfoQueue::AddApplicationMessage para**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) generar mensajes definidos por el usuario
-   La [**llamada ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) se usa para obtener mensajes (que pasan un filtro de recuperación opcional).

## <a name="registry-controls"></a>Controles del Registro

Use las claves del Registro para ajustar la configuración del filtro, ajustar los puntos de interrupción y silenciar la salida de depuración. La capa de depuración comprobará estas rutas de acceso para las claves del Registro; se usará la primera ruta de acceso encontrada.

1.  HKCU \\ Software \\ Microsoft \\ Direct3D \\<una subclave definida por el usuario>
2.  HKLM \\ Software \\ Microsoft \\ Direct3D \\<subclave definida por el usuario>
3.  HKCU \\ Software \\ Microsoft \\ Direct3D

Donde:

-   HKCU es la HKEY \_ CURRENT \_ USER y HKLM es la HKEY \_ LOCAL \_ MACHINE.
-   <una subclave definida por el> es un nombre arbitrario para almacenar la configuración de depuración de una aplicación.

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtrado de mensajes de depuración mediante claves del Registro

Si el Registro contiene una clave InfoQueueStorageFilterOverride (y no es cero), los mensajes (y la salida de depuración) se pueden filtrar agregando los siguientes controles del Registro.

-   DWORD Mute \_ \_ \* CATEGORY: salida de depuración si esta clave es distinto de cero.
-   Gravedad de exclusión \_ de DWORD: la salida de \_ \* depuración está deshabilitada si esta clave es distinta de cero.
-   Id. de exclusión mutua DWORD: se puede usar el nombre o el número del mensaje (igual que para \_ \_ \* el \* identificador breakon \_ descrito \_ \* anteriormente). La salida de depuración está deshabilitada si esta clave no es cero.
-   DWORD Unmute \_ SEVERITY \_ INFO: la salida de depuración está HABILITADA si esta clave es distinta de cero. De forma predeterminada, cuando InfoQueueStorageFilterOverride está habilitado, los mensajes de depuración con información de gravedad se silencian, por lo que esta clave permite volver a activar INFO.

Estos controles cambian si se registra o se muestra un mensaje; no afectan a si una API pasa o produce un error.

### <a name="setting-break-conditions-using-registry-keys"></a>Establecer condiciones de interrupción mediante claves del Registro

Las aplicaciones se pueden forzar a interrumpir en un mensaje mediante las siguientes claves del Registro.

**EnableBreakOnMessage:** esta clave permite la separación de mensajes (y hace que la configuración de i's SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() se ignore). Los mensajes reales en los que se van a interrumpir se definen mediante uno o varios valores BreakOn \_ \* definidos a continuación.

-   **BreakOn \_ \_CATEGORY \** _ : se interrumpirá cualquier mensaje que pase por los filtros de almacenamiento. \_ es uno de los mensajes D3D10 \_ MESSAGE \_ CATEGORY.
-   **BreakOn \_ SEVERITY \_ \** _ : se interrumpirá cualquier mensaje que pase por los filtros de almacenamiento. \_ es uno de los mensajes D3D10 \_ MESSAGE \_ \_ SEVERITY.
-   **BreakOn \_ \_ID \** _ : se interrumpirá cualquier mensaje que pase por los filtros de almacenamiento. \_ es uno de los mensajes D3D10 \_ MESSAGE ID o puede ser el valor numérico de la \_ \_ enumeración de errores. Por ejemplo, supongamos que el mensaje con el identificador "D3D10 MESSAGE ID HYPOTHETICAL" tenía el valor 123 en la enumeración ID DE \_ \_ MENSAJE \_ D3D10. \_ \_ En este caso, la creación del valor BreakOn \_ ID HYPOTHETICAL=1 o BreakOn ID 123=1 realizaría lo mismo: interrumpir cuando se encuentra un mensaje con \_ \_ \_ id. D3D10 \_ MESSAGE ID \_ \_ HYPOTHETICAL.

### <a name="muting-debug-output-using-registry-keys"></a>Muting Debug Output using Registry Keys

La salida de depuración se puede silenciar mediante una clave MuteDebugOutput. La presencia de este valor en el Registro fuerza la invalidación del método [**ID3D10InfoQueue::SetMuteDebugOutput de**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) InfoQueue. MuteDebugOutput impide que los mensajes que pasan el filtro de almacenamiento se envíen a la salida de depuración.

## <a name="disabling-debug-layer-messages"></a>Deshabilitar mensajes de capa de depuración

Los mensajes de la capa de depuración se pueden deshabilitar individualmente o como un grupo en tiempo de ejecución especificando filtros mediante [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries). El *argumento pFilter* para **ID3D10InfoQueue::AddStorageFilterEntries** toma una estructura [**D3D10 \_ INFO QUEUE \_ \_ FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) que contiene una lista de permitidos y una lista de denegación. Las listas de permitidos y denegados se describen mediante estructuras [**\_ \_ \_ \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) de filtro de cola de información D3D10 que permiten especificar el filtrado mediante el proveedor, la gravedad y el identificador de mensaje individual.

El código siguiente es un ejemplo de cómo configurar la interfaz [**ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) para denegar el mensaje D3D10 \_ MESSAGE ID DEVICE DRAW INDEX BUFFER TOO \_ \_ \_ \_ \_ \_ \_ SMALL.


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

[Capas de API](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[Características de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



