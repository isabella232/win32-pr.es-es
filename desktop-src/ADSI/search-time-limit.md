---
title: Límite de tiempo de búsqueda
description: Cuando se solicita una búsqueda en un servidor que está bajo una carga de trabajo pesada, puede que desee indicar al servidor que restrinja la búsqueda a un límite de tiempo especificado.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- ADSI de límite de tiempo de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656151"
---
# <a name="search-time-limit"></a>Límite de tiempo de búsqueda

Cuando se solicita una búsqueda en un servidor que está bajo una carga de trabajo pesada, puede que desee indicar al servidor que restrinja la búsqueda a un límite de tiempo especificado. Por ejemplo, para ejecutar una aplicación con el fin de generar un informe semanal en un servidor que ejecute casi su capacidad, y para evitar maximizar el tiempo de CPU y evitar que se ejecuten otros trabajos, puede establecer el tiempo de búsqueda en un valor pequeño y volver a ejecutar la aplicación más adelante si no puede generar el informe.

Algunos servidores pueden imponer su propio límite de tiempo administrativo. En estos casos, si especifica un valor de límite de tiempo de búsqueda mayor que el límite de tiempo administrativo, el servidor omite su especificación y usa su límite de tiempo administrativo interno en su lugar.

Para obtener más información sobre cómo usar la opción de límite de tiempo de búsqueda con una interfaz de búsqueda específica, vea:

-   [Límite de tiempo del servidor con IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

 

 




