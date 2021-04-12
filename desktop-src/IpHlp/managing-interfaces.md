---
description: La aplicación auxiliar de IP amplía sus capacidades para administrar las interfaces de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel IP, mientras que un adaptador es una abstracción de nivel de vínculo de vínculo.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Administrar interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276725"
---
# <a name="managing-interfaces"></a>Administrar interfaces

La aplicación auxiliar de IP amplía sus capacidades para administrar las interfaces de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel IP, mientras que un adaptador es una abstracción de nivel de vínculo de vínculo.

Use las funciones descritas en los párrafos siguientes para administrar interfaces en el equipo local.

La función [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) devuelve el número de interfaces en el equipo local.

La función [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) devuelve una tabla que contiene los nombres y los índices correspondientes de las interfaces en el equipo local. Para ver ejemplos de código que implican a **GetInterfaceInfo** , consulte [Administración de interfaces con GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

La función [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) toma un índice de interfaz y devuelve un índice de interfaz compatible con versiones anteriores, es decir, uno que solo usa los 24 bits inferiores. Este tipo de índice se conoce a veces como un índice de interfaz "descriptivo".

La función [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) devuelve una estructura [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) que contiene información sobre una interfaz determinada en el equipo local. Esta función requiere que el llamador proporcione el índice de la interfaz.

La función [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) devuelve una tabla de entradas [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , una para cada interfaz del equipo.

Utilice la función [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) para modificar la configuración de una interfaz determinada.

 

 
