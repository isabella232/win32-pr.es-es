---
title: Funciones de información del enrutador
description: Utilice las siguientes funciones para manipular encabezados y bloques de información del enrutador. Un encabezado de información se compone de metadatos y bloques de información privados. Los bloques de información son matrices de estructuras de información de varios tipos.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074991"
---
# <a name="router-information-functions"></a>Funciones de información del enrutador

Utilice las siguientes funciones para manipular encabezados y bloques de información del enrutador. Un encabezado de información se compone de metadatos y bloques de información privados. Los bloques de información son matrices de [estructuras de información](router-information-structures.md) de varios [tipos](router-information-enumerations.md).

Las siguientes funciones manipulan los encabezados de información:

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

Muchas de las [funciones de configuración y administración del enrutador](understanding-mprinfo-functions-and-information-headers.md) usan encabezados de información.

 

 




