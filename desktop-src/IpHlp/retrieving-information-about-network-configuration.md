---
description: La aplicación auxiliar de IP proporciona información acerca de la configuración de red del equipo local.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Recuperación de información acerca de la configuración de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002859"
---
# <a name="retrieving-information-about-network-configuration"></a>Recuperación de información acerca de la configuración de red

La aplicación auxiliar de IP proporciona información acerca de la configuración de red del equipo local. Para recuperar la información de configuración general, utilice la función [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Esta función devuelve información que no es específica de un adaptador o una interfaz concretos. Por ejemplo, **GetNetworkParams** devuelve una lista de los servidores DNS que usa el equipo local.

-   Para obtener ejemplos de código que impliquen a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , vea [recuperar información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md).

 

 



