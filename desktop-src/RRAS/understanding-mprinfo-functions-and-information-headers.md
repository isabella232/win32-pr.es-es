---
title: Descripción de las funciones de MprInfo y los encabezados de información
description: Las siguientes funciones requieren que el llamador pase una estructura o un encabezado de información como uno de los parámetros.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994291"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a>Descripción de las funciones de MprInfo y los encabezados de información

Las siguientes funciones requieren que el llamador pase una estructura o un *encabezado* de información como uno de los parámetros.



| Función de administración                                                        | Función de configuración                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Sin función de administración                                                     | [**MprConfigTransportCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [**MprAdminInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [**MprConfigInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

Del mismo modo, las siguientes funciones devuelven encabezados de información.



| Función de administración                                                        | Función de configuración                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

En el caso de las funciones de transporte, el encabezado de información contiene información global para el transporte. En el caso de las funciones de cliente (InterfaceTransport), el encabezado contiene información específica del cliente (por ejemplo, OSPF) que se administra.

Los encabezados de información y su contenido deben manipularse solo mediante las funciones de [MprInfo](router-information-functions.md) . Los desarrolladores no deben intentar manipular el contenido de los encabezados de información directamente.

Las funciones de solo interfaz, como [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , no requieren el uso de las funciones de MprInfo. La información que se pasa y se devuelve con estas funciones siempre tiene el formato de una estructura de [**\_ interfaz de MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .

 

 




