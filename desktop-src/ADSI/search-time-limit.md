---
title: Límite de tiempo de búsqueda
description: Al solicitar una búsqueda en un servidor que está bajo una carga de trabajo pesada, puede indicar al servidor que restrinja la búsqueda a un límite de tiempo especificado.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- ADSI de límite de tiempo de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b666b41db67872cd418cca2d4ef2e3d766fbc1a1d1c1a2d9945eec7dfceb2429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690520"
---
# <a name="search-time-limit"></a>Límite de tiempo de búsqueda

Al solicitar una búsqueda en un servidor que está bajo una carga de trabajo pesada, puede indicar al servidor que restrinja la búsqueda a un límite de tiempo especificado. Por ejemplo, para ejecutar una aplicación para generar un informe semanal en un servidor que se ejecuta cerca de la capacidad y para evitar maximizar el tiempo de CPU e impedir que se ejecuten otros trabajos, puede establecer el tiempo de búsqueda en un valor pequeño y volver a ejecutar la aplicación más adelante si no se puede generar el informe.

Algunos servidores pueden imponer su propio límite de tiempo administrativo. En estos casos, si especifica un valor de límite de tiempo de búsqueda mayor que el límite de tiempo administrativo, el servidor omite la especificación y usa su límite de tiempo administrativo interno en su lugar.

Para obtener más información sobre el uso de la opción de límite de tiempo de búsqueda con una interfaz de búsqueda específica, vea:

-   [Límite de tiempo del servidor con IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Buscar con ActiveX objetos de datos](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

 

 




