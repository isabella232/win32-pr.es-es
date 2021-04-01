---
description: Objetos de proveedor de software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Objetos de proveedor de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913953"
---
# <a name="software-provider-objects"></a>Objetos de proveedor de software

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Los objetos de proveedor de software modelan dispositivos físicos, como discos IDE y CD-ROM, y elementos virtuales como paquetes, volúmenes y complejos de volumen. En la ilustración siguiente se muestra la relación entre el objeto de proveedor y el conjunto de objetos de proveedor de software, así como la relación entre los distintos objetos de proveedor de software.

![Diagrama que muestra la relación entre un ' proveedor ' y objetos de proveedor de software, como ' Pack ' y ' volumen '.](images/vdsswobjects.png)

Un objeto de proveedor puede contener cero o más paquetes. Un objeto de paquete puede contener cero o más volúmenes y discos. Un volumen consta de al menos un Plex de volumen y cada Plex de volumen se puede asignar a uno o varios discos, dependiendo del tipo de Plex. VDS administra los discos sin asignar directamente, sin un contenedor de paquetes. En los temas restantes de esta sección se describen los objetos de paquete, disco, volumen y volumen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> </dl>

 

 
