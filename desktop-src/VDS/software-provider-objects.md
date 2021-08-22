---
description: Objetos de proveedor de software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Objetos de proveedor de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507abb00b67b51ad68eb0592ff4fa7b5201cff5be0587b7170662556238feb50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137167"
---
# <a name="software-provider-objects"></a>Objetos de proveedor de software

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [de Virtual Disk Service](virtual-disk-service-portal.md) se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Los objetos de proveedor de software modelan dispositivos físicos, como discos IDE y CD-ROMs, y elementos virtuales como paquetes, volúmenes y plexos de volumen. En la ilustración siguiente se muestra la relación entre el objeto de proveedor y el conjunto de objetos de proveedor de software, así como la relación entre los distintos objetos de proveedor de software.

![Diagrama que muestra la relación entre un objeto 'Provider' y los objetos de proveedor de software, como 'Pack' y 'Volume'.](images/vdsswobjects.png)

Un objeto de proveedor puede contener cero o más paquetes. Un objeto pack puede contener cero o más discos y volúmenes. Un volumen consta de al menos un plex de volumen y cada plex de volumen se puede asignar a uno o varios discos, según el tipo de plex. VDS administra los discos sin asignar directamente, sin un contenedor de paquetes. En los temas restantes de esta sección se describen los objetos pack, disk, volume y volume plex.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> </dl>

 

 
