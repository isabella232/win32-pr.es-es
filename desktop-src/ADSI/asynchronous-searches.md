---
title: Búsquedas asincrónicas
description: La habilitación de los resultados de búsqueda asincrónicos (asincrónicos) en una llamada a GetFirstRow o la primera llamada a GetNextRow se bloquea hasta que la primera entrada se devuelve desde el servidor.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- ADSI búsquedas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993872"
---
# <a name="asynchronous-searches"></a>Búsquedas asincrónicas

La habilitación de los resultados de búsqueda asincrónicos (asincrónicos) en una llamada a **GetFirstRow** o la primera llamada a **GetNextRow** se bloquea hasta que la primera entrada se devuelve desde el servidor. Es decir, si la búsqueda en el servidor requiere mucho tiempo, los primeros resultados se devuelven rápidamente. Esto puede ayudar al rellenar un cuadro de lista con los resultados de la búsqueda. Los resultados de la búsqueda se muestran a medida que se devuelven.

Si Async está deshabilitado, la primera llamada a **GetFirstRow** o **GetNextRow** se bloqueará hasta que el servidor calcule todo el conjunto de resultados y devuelva. Solo entonces es la primera fila devuelta. Esto no se recomienda si se espera que el conjunto de resultados sea grande.

Si tanto la paginación como la asincrónica están habilitadas, la primera llamada a **GetFirstRow** o **GetNextRow** se bloqueará hasta que el servidor genere y envíe la primera página de resultados. Si se ha establecido un tamaño de Página razonable, los resultados aparecerán inmediatamente. Lo que es más importante, si se espera que los resultados de la búsqueda sean muy grandes y busca una entrada determinada, no es necesario que solicite más resultados del servidor una vez que haya encontrado las entradas que le interesen.

Una búsqueda asincrónica paginada proporciona un control exhaustivo de una búsqueda. Esto resulta útil si los resultados de la búsqueda pueden ser muy grandes y requieren mucho tiempo desde el servidor.

Para obtener más información sobre el uso de búsquedas asincrónicas con una interfaz de búsqueda específica, vea:

-   [Búsquedas sincrónicas y asincrónicas con IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

 

 




