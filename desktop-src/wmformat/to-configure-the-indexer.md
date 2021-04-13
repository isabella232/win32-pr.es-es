---
title: Para configurar el indexador
description: Para configurar el indexador
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- SDK de Windows Media Format, configurar indexadores
- Advanced Systems Format (ASF), configurar indexadores
- ASF (formato de sistemas avanzados), configurar indexadores
- índices, configurar indexadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420295"
---
# <a name="to-configure-the-indexer"></a>Para configurar el indexador

Puede configurar el indexador antes de usarlo para indizar un archivo ASF. Cada secuencia del archivo puede configurarse por separado, o bien puede establecer la misma configuración para todos los flujos.

Si está configurando varias transmisiones para la indexación en un archivo, debe configurarlas todas y, a continuación, comenzar la indexación. Si configura e indexa una secuencia y, a continuación, configura otra secuencia en el mismo archivo, si vuelve a iniciar el indexador, se eliminará el primer índice. Esto es para cumplir con el formato de archivo ASF.

En el código siguiente se muestra cómo configurar el indizador. El código presupone que el archivo que se va a indexar tiene dos flujos: el primero es una secuencia de audio que no necesita indexarse y el segundo es una secuencia de vídeo. Este código solo muestra cómo configurar el indizador. Para indexar un archivo, debe seguir los pasos que se describen en [para indizar un archivo ASF](to-index-an-asf-file.md).


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> El tipo de índice predeterminado es WMT es el \_ \_ \_ punto limpio más cercano \_ . Aunque puede establecer el tipo de índice en otros valores, al hacerlo se reducirá el rendimiento de búsqueda.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMIndexer2:: configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**Para indexar un archivo ASF**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




