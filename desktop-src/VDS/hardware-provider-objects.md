---
description: Objetos de proveedor de hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Objetos de proveedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890393"
---
# <a name="hardware-provider-objects"></a>Objetos de proveedor de hardware

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

El modelo de objetos VDS incluye un conjunto de objetos para consultar y configurar entidades de proveedor de hardware. (Tenga en cuenta que, aunque VDS incluye un proveedor de software, debe adquirir un proveedor de hardware y el hardware asociado por separado para aprovechar las ventajas de los objetos del proveedor de hardware). Estos objetos de proveedor de hardware representan dispositivos físicos (como subsistemas, unidades y controladores) y dispositivos virtuales (como LUN y plexos LUN).

Un proveedor de hardware debe crear un objeto COM para cada dispositivo físico o virtual.

En la ilustración siguiente se muestra la relación entre el objeto de proveedor y el conjunto de objetos de proveedor de hardware, así como la relación entre los distintos objetos del proveedor de hardware.

![Diagrama que muestra la relación entre "Provider" y "Subsystem", "Controller", "LUN", "LUN plex", "Drive" y "Subsystem". ](images/vdshwobjects.png)

Un objeto de proveedor puede contener cualquier número de subsistemas. Todos los proveedores de hardware son capaces de administrar varias instancias del mismo modelo de subsistema. Muchos proveedores de hardware también son capaces de administrar varias instancias de diferentes modelos de subsistema. Un único equipo puede hospedar cualquier número de proveedores de hardware.

Un objeto de subsistema puede contener cualquier número de controladores y unidades, y puede superficier cualquier número de LUN. Un objeto LUN consta de al menos un plex LUN y cada plex LUN se asigna a una o más unidades, según el tipo de plex. Los objetos de controlador pueden administrar la entrada y salida de datos para cualquier número de objetos LUN.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> </dl>

 

 
