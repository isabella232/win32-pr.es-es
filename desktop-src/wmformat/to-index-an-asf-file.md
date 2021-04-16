---
title: Para indexar un archivo ASF
description: Para indexar un archivo ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, indexación de archivos ASF
- Advanced Systems Format (ASF), indexación de archivos
- ASF (formato de sistemas avanzados), indexación de archivos
- índices, indexación de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105685677"
---
# <a name="to-index-an-asf-file"></a>Para indexar un archivo ASF

El proceso de indización de un archivo ASF es muy sencillo. Realice una llamada a [**IWMIndexer:: StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) y pase el nombre de archivo. El indexador realiza el resto. La llamada a **StartIndexing** es asincrónica, por lo que el estado debe supervisarse mediante la devolución de llamada de **Estado** .

En el código siguiente se muestra cómo indizar un archivo ASF. Si desea configurar el indexador antes de indizar el archivo, deberá incluir el código del ejemplo incluido en [para configurar el indizador](to-configure-the-indexer.md).

En este ejemplo, el identificador que señala al evento debe crearse como una variable global para que sea accesible para la devolución de llamada. La siguiente declaración debe aparecer en un ámbito global.


```C++
HANDLE g_hEvent = NULL;

```



En un escenario más realista, el identificador de evento debe ser un miembro de datos de la clase que contiene la devolución de llamada y la lógica para iniciar el indizador.

El indexador envía varios eventos a la devolución de llamada de **Estado** después de la llamada a **IWMIndexer:: StartIndexing**. Puede interceptarlos según sea necesario para la aplicación. Como mínimo, debe interceptar \_ el cierre de WMT, que se envía cuando se completa la indexación. Use la siguiente lógica en el conmutador de mensajes en la implementación de la devolución de llamada de **Estado** .


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



En este ejemplo se supone que se tiene acceso a la implementación de la devolución de llamada en **Estado** a través de un objeto denominado DoCallBack. Para obtener más información sobre el uso de eventos y devoluciones de llamada con este SDK, vea [usar los métodos de devolución de llamada](using-the-callback-methods.md).


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Para configurar el indexador**](to-configure-the-indexer.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




