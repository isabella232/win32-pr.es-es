---
title: Eliminar un cliente de una interfaz
description: Para eliminar un cliente, como un protocolo de enrutamiento, de una interfaz determinada, use MprAdminInterfaceTransportGetInfo o MprConfigInterfaceTransportGetInfo para recuperar toda la información del cliente de la interfaz.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585a37920b59f47a0c933427d7218d08a61bed9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994389"
---
# <a name="deleting-a-client-from-an-interface"></a>Eliminar un cliente de una interfaz

Para eliminar un cliente, como un protocolo de enrutamiento, de una interfaz determinada, use [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) o [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) para recuperar toda la información del cliente de la interfaz. Use [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) para quitar el bloque de información del cliente que se va a eliminar. A continuación, use [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) para agregar un bloque de longitud cero para que se elimine el cliente. Por último, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) o [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) para volver a guardar la información en el enrutador en ejecución o en el registro.

Si el administrador de enrutadores recibe un bloque de información de la interfaz de longitud cero para un cliente, sabe eliminar ese cliente de la interfaz. El administrador de enrutador elimina el cliente mediante una llamada a la implementación del cliente de [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface). Tenga en cuenta la diferencia importante entre pasar un encabezado de información que no contenga un bloque de información para un cliente y pasar un encabezado de información que contenga un bloque de información de longitud cero para el cliente. En el primer caso, el administrador de enrutadores no realiza ninguna acción con respecto al cliente. En el segundo caso, el administrador de enrutadores elimina el cliente de la interfaz.

 

 




