---
title: Tiempo de espera de búsqueda
description: Un cliente también puede imponer un límite de tiempo que esperará a que un servidor devuelva el conjunto de resultados.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- ADSI de tiempo de espera de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99b287c1bc0ba0da5e39b579c4a454eae821cf2c443930a5ae0376412e2c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082309"
---
# <a name="search-time-out"></a>Tiempo de espera de búsqueda

Un cliente también puede imponer un límite de tiempo que esperará a que un servidor devuelva el conjunto de resultados. El valor de la opción "tiempo de espera de búsqueda" especifica este límite. Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede detener la búsqueda e intentarlo de nuevo más adelante.

La propiedad de tiempo de espera es útil cuando un cliente solicita una búsqueda asincrónica. En una búsqueda asincrónica, el cliente realiza una solicitud y, a continuación, continúa con otras tareas mientras espera a que el servidor devuelva los resultados. Es posible que el servidor pueda desconectarse sin notificar al cliente. En este caso, el cliente no tiene ninguna manera de reconocer que el servidor sigue procesando la consulta o si ha dejado de estar en directo. La propiedad de tiempo de espera proporciona al cliente cierto control en tales instancias.

Para obtener más información sobre el uso de la opción de tiempo de espera de búsqueda con una interfaz de búsqueda específica, vea:

-   [Límite de tiempo de cliente con IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Buscar con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
-   [Búsqueda con OLE DB](searching-with-ole-db.md)

 

 




