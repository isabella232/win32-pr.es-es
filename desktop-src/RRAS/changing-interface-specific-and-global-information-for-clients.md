---
title: Cambio de la información global y Interface-Specific de los clientes
description: Para cambiar la información de la interfaz de un cliente específico, por ejemplo, NAT, use primero el correspondiente \ 0034; GetInfo \ 0034; función para recuperar la información actual.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c8f2ef3c37d75db1cc7686a67108530b16b28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994228"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Cambio de la información global y Interface-Specific de los clientes

Para cambiar la información de la interfaz de un cliente específico, por ejemplo NAT, use primero la función "GetInfo" adecuada para recuperar la información actual. Si el enrutador se está ejecutando, use [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Si el enrutador no se está ejecutando, use [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Esta llamada recupera la información de todos los clientes que se ejecutan en la interfaz especificada. Por ejemplo, si tanto OSPF como RIP se están ejecutando en una interfaz determinada, esta llamada recupera la información de la interfaz para ambos. Utilice la función [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) para buscar el bloque de información que corresponde al cliente que desea modificar. A continuación, utilice la función [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) para realizar las modificaciones. Por último, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) o [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) para realizar los cambios en el enrutador en ejecución o la configuración del enrutador en el registro.

La información de cliente global es información que no es específica de ninguna interfaz determinada en la que el cliente se está ejecutando. Use un procedimiento similar para modificar la información global de un cliente específico. En primer lugar, recupere la información global de todos los clientes que usan [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) o [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo). A continuación, use las funciones de MprInfo para modificar la información. Por último, use las funciones [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) o [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) para guardar la información modificada en el enrutador en ejecución o en el registro.

Las llamadas a las funciones de administración anteriores pasan por el administrador de interfaz dinámica (DIM) y, finalmente, se convierten en llamadas desde el administrador de enrutadores a los propios clientes. Todos los clientes, sean o no protocolos de enrutamiento, deben ajustarse a la interfaz descrita en la sección [interfaz del Protocolo de enrutador](about-routing-protocol-interface.md). Como parte de esta interfaz, el protocolo de enrutamiento debe admitir las siguientes funciones (entre otras):

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

El administrador de enrutadores llama a las funciones de [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) para cada uno de los clientes para recopilar la información que se devuelve de una llamada a [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Del mismo modo, cuando el administrador de enrutadores recibe información actualizada a través de la llamada [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) , usa las funciones [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) para actualizar la información de la interfaz para cada uno de los clientes.

 

 




