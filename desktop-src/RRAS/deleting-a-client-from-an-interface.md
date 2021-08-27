---
title: Eliminación de un cliente de una interfaz
description: Para eliminar un cliente, como un protocolo de enrutamiento, de una interfaz determinada, use MprAdminInterfaceTransportGetInfo o MprConfigInterfaceTransportGetInfo para recuperar toda la información de cliente de la interfaz.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e5b93e062f5971f6e43ad1d7c08f7a0c2ef3bff72e66849815a053b342b13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127895"
---
# <a name="deleting-a-client-from-an-interface"></a>Eliminación de un cliente de una interfaz

Para eliminar un cliente, como un protocolo de enrutamiento, de una interfaz determinada, use [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) o [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) para recuperar toda la información de cliente de la interfaz. Use [**MprInfoBlockRemove para**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) quitar el bloque de información del cliente que se va a eliminar. A [**continuación, use MprInfoBlockAdd para**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) agregar un bloque de longitud cero para que el cliente se elimine. Por último, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) [**o MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) para guardar la información en el enrutador en ejecución o en el Registro.

Si el administrador de enrutadores recibe un bloque de información de interfaz de longitud cero para un cliente, sabe que elimina ese cliente de la interfaz. El administrador de enrutadores elimina el cliente mediante una llamada a la implementación del cliente de [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface). Tenga en cuenta la distinción importante entre pasar un encabezado de información que no contiene un bloque de información para un cliente y pasar un encabezado de información que contenga un bloque de información de longitud cero para el cliente. En el primer caso, el administrador de enrutadores no realiza ninguna acción con respecto al cliente. En el segundo caso, el administrador de enrutadores elimina el cliente de la interfaz.

 

 




