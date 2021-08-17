---
title: Cambiar Interface-Specific e información global para clientes
description: Para cambiar la información de interfaz de un cliente específico, por ejemplo NAT, use primero el valor adecuado \ 0034; GetInfo \ 0034; función para recuperar la información actual.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcea02c6d70e7d7e2da53926854879f1ca5b76526a83185b786b0074b8098434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791758"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Cambiar Interface-Specific e información global para clientes

Para cambiar la información de interfaz de un cliente específico, por ejemplo NAT, use primero la función "GetInfo" adecuada para recuperar la información actual. Si el enrutador se está ejecutando, use [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Si el enrutador no se está ejecutando, use [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Esta llamada recupera la información de todos los clientes que se ejecutan en la interfaz especificada. Por ejemplo, si OSPF y RIP se ejecutan en una interfaz determinada, esta llamada recupera la información de interfaz para ambos. Use la [**función MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) para buscar el bloque de información que corresponde al cliente que desea modificar. A continuación, [**use la función MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) para realizar las modificaciones. Por último, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) o [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) para realizar los cambios en el enrutador en ejecución o en la configuración del enrutador en el Registro.

La información de cliente global es información que no es específica de ninguna interfaz determinada en la que se ejecuta el cliente. Use un procedimiento similar para modificar la información global de un cliente específico. En primer lugar, recupere la información global de todos los clientes mediante [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) [**o MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo). A continuación, use las funciones MprInfo para modificar la información. Por último, use las funciones [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) o [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) para guardar la información modificada en el enrutador en ejecución o en el Registro.

Las llamadas a las funciones de administración anteriores pasan a través del Administrador de interfaces dinámicas (DIM) y, finalmente, se traducen en llamadas del administrador de enrutadores a los propios clientes. Todos los clientes, tanto si son protocolos de enrutamiento como si no, deben ajustarse a la interfaz descrita en la sección Interfaz del [protocolo de enrutador](about-routing-protocol-interface.md). Como parte de esta interfaz, el protocolo de enrutamiento debe admitir las siguientes funciones (entre otras):

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

El administrador de enrutadores llama a las funciones [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) de cada uno de los clientes para recopilar la información que se devuelve de una llamada a [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). De forma similar, cuando el administrador de enrutadores recibe información actualizada a través de una llamada [**a MprAdminInterfaceTransportSetInfo,**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) usa las funciones [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) para actualizar la información de interfaz de cada uno de los clientes.

 

 




