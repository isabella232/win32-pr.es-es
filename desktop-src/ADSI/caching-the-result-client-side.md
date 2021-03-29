---
title: Almacenar en caché el resultado (cliente)
description: El almacenamiento en caché del lado cliente almacena el conjunto de resultados en la memoria del cliente, lo que proporciona mejoras de rendimiento para el lado cliente.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Almacenar en caché el resultado (cliente) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993867"
---
# <a name="caching-the-result-client-side"></a>Almacenar en caché el resultado (cliente)

El almacenamiento en caché del lado cliente almacena el conjunto de resultados en la memoria del cliente, lo que proporciona mejoras de rendimiento para el lado cliente. Un cliente puede volver a visitar un objeto varias veces sin necesidad de varios recorridos al servidor. De forma predeterminada, ADSI almacena en caché el conjunto de resultados de los clientes. Esto permite a ADSI proporcionar a los clientes compatibilidad con cursores de tipo SQL. Puede recorrer en iteración un conjunto de resultados determinado varias veces.

ADSI también permite a los clientes desactivar la memoria caché para reducir los requisitos de memoria. Si el almacenamiento en caché del lado cliente está deshabilitado, el cliente no mantiene el conjunto de resultados en la memoria. Cada fila se libera una vez que la aplicación la recupera. Deshabilitar el almacenamiento en caché del lado cliente puede ser útil para reducir los requisitos de memoria del lado cliente en tales casos, como cuando solo se desea realizar un único paso a través del conjunto de resultados. Sin embargo, cuando los clientes optan por no almacenar en caché el resultado, proporcionan compatibilidad con los cursores.

Para obtener más información sobre el almacenamiento en caché de resultados con una interfaz de búsqueda específica, vea:

-   [Almacenamiento en caché de resultados con IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

 

 




