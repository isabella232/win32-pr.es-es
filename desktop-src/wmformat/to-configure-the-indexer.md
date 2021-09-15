---
title: Para configurar el indexador
description: Para configurar el indexador
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows SDK de formato multimedia, configuración de indexadores
- Formato de sistemas avanzados (ASF), configuración de indexadores
- ASF (formato de sistemas avanzados), configuración de indexadores
- indexes,configuring indexers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571237"
---
# <a name="to-configure-the-indexer"></a>Para configurar el indexador

Puede configurar el indexador antes de usarlo para indexar un archivo ASF. Cada secuencia del archivo se puede configurar por separado o puede establecer la misma configuración para todas las secuencias.

Si va a configurar varios puertos para la indexación en un archivo, debe configurarlos todos y, a continuación, comenzar la indexación. Si configura e indexa una secuencia y, a continuación, configura otra secuencia en el mismo archivo, al iniciar de nuevo el indexador se eliminará el primer índice. Esto es para cumplir con el formato de archivo ASF.

El código siguiente muestra cómo configurar el indexador. El código supone que el archivo que se va a indexar tiene dos secuencias: la primera es una secuencia de audio que no es necesario indexar y la segunda es una secuencia de vídeo. Este código muestra solo cómo configurar el indexador. Para indexar un archivo, debe seguir los pasos que se presentan en [Para indexar un archivo ASF](to-index-an-asf-file.md).


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
> El tipo de índice predeterminado es WMT \_ IT \_ NEAREST CLEAN \_ \_ POINT. Aunque puede establecer el tipo de índice en otros valores, al hacerlo se degradará el rendimiento de la búsqueda.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**Para indexar un archivo ASF**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




