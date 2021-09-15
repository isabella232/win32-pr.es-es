---
description: La interfaz de programación ad hoc inalámbrica se compone de las interfaces siguientes.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Interfaces ad hoc inalámbricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473728"
---
# <a name="wireless-ad-hoc-interfaces"></a>Interfaces ad hoc inalámbricas

La interfaz de programación ad hoc inalámbrica se compone de las interfaces siguientes.



| Nombre de la interfaz                                                                       | Descripción                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | Representa una tarjeta de interfaz de red inalámbrica (NIC).                                                    |
| [**IDot11AdHocInterfaceNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | Define las notificaciones admitidas por [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).           |
| [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | Crea y administra redes ad hoc 802.11.                                                            |
| [**IDot11AdHocManagerNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | Define las notificaciones admitidas por la [**interfaz IDot11AdHocManager.**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) |
| [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | Representa un destino de red ad hoc disponible dentro del intervalo de conexión.                            |
| [**IDot11AdHocNetworkNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | Define las notificaciones admitidas por la [**interfaz IDot11AdHocNetwork.**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) |
| [**IDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | Especifica la configuración de seguridad de una red ad hoc inalámbrica.                                         |
| [**IEnumDot11AdHocInterfaces**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | Representa la colección de interfaces de red ad hoc 802.11 visibles actualmente.                       |
| [**IEnumDot11AdHocNetworks**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | Representa la colección de redes ad hoc 802.11 visibles actualmente.                                 |
| [**IEnumDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | Representa la colección de configuraciones de seguridad asociadas a cada red ad hoc inalámbrica visible.   |



 

> [!Note]  
> Es posible que el modo ad hoc no esté disponible en versiones futuras de Windows. A partir de Windows 8.1 y Windows Server 2012 R2, use Wi-Fi Direct en [su lugar.](about-the-wi-fi-direct-api.md)

 

 

 



