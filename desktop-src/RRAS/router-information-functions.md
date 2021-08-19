---
title: Funciones de información del enrutador
description: Use las siguientes funciones para manipular los encabezados y bloques de información del enrutador. Un encabezado de información se compone de metadatos privados y bloques de información. Los bloques de información son matrices de estructuras de información de varios tipos.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029b36ef862f11c58492fd8ec9c7c6f292797c2e35e75592f385e18d6d0e1a25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788020"
---
# <a name="router-information-functions"></a>Funciones de información del enrutador

Use las siguientes funciones para manipular los encabezados y bloques de información del enrutador. Un encabezado de información se compone de metadatos privados y bloques de información. Los bloques de información son matrices [de estructuras de información](router-information-structures.md) de varios [tipos.](router-information-enumerations.md)

Las siguientes funciones manipulan encabezados de información:

-   [**MprInfoCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [**MprInfoDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [**MprInfoDuplicate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [**MprInfoRemoveAll**](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

Las siguientes funciones manipulan bloques de información dentro de un encabezado de información:

-   [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [**MprInfoBlockQuerySize**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

Muchas de las funciones [de configuración y administración del enrutador](understanding-mprinfo-functions-and-information-headers.md) usan encabezados de información.

 

 




