---
title: Para detener la indización en curso
description: Para detener la indización en curso
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- SDK de Windows Media Format, detener la indexación en curso
- Advanced Systems Format (ASF), detener la indexación en curso
- ASF (formato de sistemas avanzados), detener la indexación en curso
- índices, detener la indexación en curso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077338"
---
# <a name="to-stop-indexing-in-progress"></a>Para detener la indización en curso

Después de comenzar la indexación con una llamada a [**IWMIndexer:: StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), el indizador continuará normalmente hasta que se indexe el archivo. Puede detener las operaciones de indización mediante una llamada al método [**IWMIndexer:: CANCEL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) . Una vez cancelada la indexación, puede volver a llamar a **StartIndexing** , pero el indexador comenzará desde el principio del archivo en lugar de reanudarse desde el punto de cancelación.

Dado que **StartIndexing** es una llamada asincrónica, normalmente necesitará llamar a **Cancel** desde otro subproceso o controlador de eventos de la aplicación. Normalmente se llama a **Cancel** desde un procedimiento de evento asociado a un control de botón de una aplicación Windows.

Cuando se cancela la indexación, el indexador pasará un mensaje de estado de WMT \_ cerrado, como si el archivo se hubiera indizado correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




