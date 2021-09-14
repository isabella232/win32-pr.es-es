---
description: Objetos de proveedor de software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Objetos de proveedor de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170598"
---
# <a name="software-provider-objects"></a>Objetos de proveedor de software

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM [del](virtual-disk-service-portal.md) servicio virtual de disco se reemplaza [por el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Los objetos de proveedor de software modelan dispositivos físicos, como discos IDE y CD-ROM, y elementos virtuales como paquetes, volúmenes y plexos de volumen. En la ilustración siguiente se muestra la relación entre el objeto de proveedor y el conjunto de objetos de proveedor de software, así como la relación entre los distintos objetos de proveedor de software.

![Diagrama que muestra la relación entre un 'proveedor' y objetos de proveedor de software, como 'Pack' y 'Volume'.](images/vdsswobjects.png)

Un objeto de proveedor puede contener cero o más paquetes. Un objeto pack puede contener cero o más discos y volúmenes. Un volumen consta de al menos un plex de volumen y cada plex de volumen se puede asignar a uno o varios discos, según el tipo de plex. VDS administra los discos sin asignar directamente, sin un contenedor pack. En los temas restantes de esta sección se describen los objetos pack, disk, volume y volume plex.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> </dl>

 

 
