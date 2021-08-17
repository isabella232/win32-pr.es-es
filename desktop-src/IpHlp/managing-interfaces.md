---
description: El asistente de IP amplía sus capacidades para administrar interfaces de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel de IP, mientras que un adaptador es una abstracción de nivel de vínculo de datos.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Administración de interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb46ecba6f1c5780960f6d8e363db9ec04d0cc3611da1caf023ec95bf5a99a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146698"
---
# <a name="managing-interfaces"></a>Administración de interfaces

El asistente de IP amplía sus capacidades para administrar interfaces de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel de IP, mientras que un adaptador es una abstracción de nivel de vínculo de datos.

Use las funciones descritas en los párrafos siguientes para administrar interfaces en el equipo local.

La [**función GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) devuelve el número de interfaces en el equipo local.

La [**función GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) devuelve una tabla que contiene los nombres y los índices correspondientes para las interfaces del equipo local. Para obtener ejemplos de código **que implican GetInterfaceInfo,** vea [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

La [**función GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) toma un índice de interfaz y devuelve un índice de interfaz compatible con versiones anteriores, es decir, uno que usa solo los 24 bits inferiores. Este tipo de índice se conoce a veces como índice de interfaz "descriptivo".

La [**función GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) devuelve una [**estructura \_ IFROW de MIB**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) que contiene información sobre una interfaz determinada en el equipo local. Esta función requiere que el autor de la llamada proporcione el índice de la interfaz .

La [**función GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) devuelve una tabla de entradas [**\_ IFROW de MIB,**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) una para cada interfaz del equipo.

Use la [**función SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) para modificar la configuración de una interfaz determinada.

 

 
