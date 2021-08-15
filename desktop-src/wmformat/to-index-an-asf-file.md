---
title: Para indexar un archivo ASF
description: Para indexar un archivo ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows SDK de formato multimedia, indexación de archivos ASF
- Formato de sistemas avanzados (ASF), archivos de indexación
- ASF (formato de sistemas avanzados), archivos de indexación
- índices, indexación de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c2e41ed60ecb8fcee39da35dbc79ec44cece8db62f3e040d42aee3374c5690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845583"
---
# <a name="to-index-an-asf-file"></a>Para indexar un archivo ASF

El proceso de indexación de un archivo ASF es muy sencillo. Realice una llamada a [**IWMIndexer::StartIndexing y**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) pase el nombre de archivo. El indexador hace el resto. La llamada a **StartIndexing** es asincrónica, por lo que el estado debe supervisarse mediante la devolución **de llamada OnStatus.**

El código siguiente muestra cómo indexar un archivo ASF. Si desea configurar el indexador antes de indexar el archivo, deberá incluir código del ejemplo incluido en Para configurar [el indexador.](to-configure-the-indexer.md)

En este ejemplo, el identificador que apunta al evento debe crearse como una variable global para que sea accesible mediante la devolución de llamada. La siguiente declaración debe aparecer en un ámbito global.


```C++
HANDLE g_hEvent = NULL;

```



En un escenario más realista, el identificador de eventos debe ser un miembro de datos de la clase que contiene la devolución de llamada y la lógica para iniciar el indexador.

El indexador envía varios eventos a la devolución de llamada **OnStatus** después de la llamada a **IWMIndexer::StartIndexing**. Puede capturarlos según sea necesario para la aplicación. Como mínimo, debe capturar WMT \_ CLOSED, que se envía cuando se completa la indexación. Use la siguiente lógica dentro del modificador de mensaje en la implementación de la **devolución de llamada OnStatus.**


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



En este ejemplo se supone que se tiene acceso a la implementación de la devolución de llamada **OnStatus** a través de un objeto denominado MyCallback. Para obtener más información sobre el uso de eventos y devoluciones de llamada con este SDK, vea [Usar los métodos de devolución de llamada](using-the-callback-methods.md).


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

[**IWMIndexer (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Para configurar el indexador**](to-configure-the-indexer.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




