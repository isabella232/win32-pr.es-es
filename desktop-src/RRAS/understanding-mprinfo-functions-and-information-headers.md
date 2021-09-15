---
title: Descripción de las funciones mprInfo y los encabezados de información
description: Las funciones siguientes requieren que el autor de la llamada pase una estructura de información o un encabezado como uno de los parámetros.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476633"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a>Descripción de las funciones mprInfo y los encabezados de información

Las funciones siguientes requieren que el autor de la llamada pase una estructura de información o *un encabezado* como uno de los parámetros.



| Función de administración                                                        | Función de configuración                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Sin función de administración                                                     | [**MprConfigTransportCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [**MprAdminInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [**MprConfigInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

De forma similar, las siguientes funciones devuelven encabezados de información.



| Función de administración                                                        | Función de configuración                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

Para las funciones de transporte, el encabezado de información contiene información global para el transporte. Para las funciones de cliente (InterfaceTransport), el encabezado contiene información específica del cliente (por ejemplo, OSPF) que se administra.

Los encabezados de información y su contenido solo deben manipularse mediante las [funciones MprInfo.](router-information-functions.md) Los desarrolladores no deben intentar manipular directamente el contenido de los encabezados de información.

Las funciones solo de interfaz, [**como MprAdminInterfaceSetInfo,**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) no requieren el uso de funciones MprInfo. La información que se pasa y devuelve con estas funciones siempre tiene el formato de una estructura [**\_ DE INTERFAZ DE MPR.**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)

 

 




