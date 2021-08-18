---
title: Búsquedas asincrónicas
description: Al habilitar la búsqueda asincrónica (asincrónica), se produce una llamada a GetFirstRow o la primera llamada a GetNextRow se bloquea hasta que se devuelve la primera entrada desde el servidor.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Búsquedas asincrónicas ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bca36a30b3b0a46f983da54ecaee753a4b15a455b0e69f9399eacdec68aecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082789"
---
# <a name="asynchronous-searches"></a>Búsquedas asincrónicas

Al habilitar la búsqueda asincrónica (asincrónica), se produce una llamada a **GetFirstRow** o la primera llamada a **GetNextRow** se bloquea hasta que se devuelve la primera entrada desde el servidor. Es decir, si la búsqueda en el servidor requiere mucho tiempo, los primeros resultados se devuelven rápidamente. Esto puede ser de ayuda al rellenar un cuadro de lista con resultados de búsqueda. Los resultados de la búsqueda se muestran a medida que se devuelven.

Si async está deshabilitado, la primera llamada a **GetFirstRow** o **GetNextRow** se bloqueará hasta que el servidor calcule todo el conjunto de resultados y devuelva. Solo entonces se devuelve la primera fila. Esto no se recomienda si se espera que el conjunto de resultados sea grande.

Si tanto la paginación como la asincrónica están habilitadas, la primera llamada a **GetFirstRow** o **GetNextRow** se bloqueará hasta que el servidor genere y envíe la primera página de resultados. Si se estableció un tamaño de página razonable, los resultados aparecerán inmediatamente. Lo que es más importante, si se espera que los resultados de la búsqueda sean muy grandes y busque una entrada determinada, no es necesario que solicite más resultados al servidor después de haber encontrado las entradas que le interesan.

Una búsqueda asincrónica paginada proporciona un control preciso de una búsqueda. Esto resulta útil si los resultados de la búsqueda pueden ser muy grandes y requieren mucho tiempo del servidor.

Para obtener más información sobre el uso de búsquedas asincrónicas con una interfaz de búsqueda específica, vea:

-   [Búsquedas sincrónicas y asincrónicas con IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Buscar con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

 

 




