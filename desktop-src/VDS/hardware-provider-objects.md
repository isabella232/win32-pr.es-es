---
description: Objetos de proveedor de hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Objetos de proveedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105697902"
---
# <a name="hardware-provider-objects"></a>Objetos de proveedor de hardware

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

El modelo de objetos de VDS incluye un conjunto de objetos para consultar y configurar entidades de proveedor de hardware. (Tenga en cuenta que, aunque VDS incluye un proveedor de software, debe adquirir un proveedor de hardware y el hardware asociado por separado para aprovechar las ventajas de los objetos de proveedor de hardware). Estos objetos de proveedor de hardware representan dispositivos físicos (como subsistemas, unidades y controladores) y dispositivos virtuales (como LUN y complejos de LUN).

Un proveedor de hardware debe crear un objeto COM para cada dispositivo físico o virtual.

La ilustración siguiente muestra la relación entre el objeto de proveedor y el conjunto de objetos de proveedor de hardware, así como la relación entre los distintos objetos de proveedor de hardware.

![Diagrama que muestra la relación entre el ' proveedor ' y el ' subsistema ', ' controlador ', ' LUN ', ' LUN Plex ', ' Drive ' y ' eje '. ](images/vdshwobjects.png)

Un objeto de proveedor puede contener cualquier número de subsistemas. Todos los proveedores de hardware pueden administrar varias instancias del mismo modelo de subsistema. Muchos proveedores de hardware también pueden administrar varias instancias de diferentes modelos de subsistema. Un solo equipo puede hospedar cualquier número de proveedores de hardware.

Un objeto de subsistema puede contener cualquier número de controladores y unidades, y puede mostrar cualquier número de LUN. Un objeto LUN se compone de al menos un Plex de LUN y cada complejo de LUN se asigna a una o más unidades, dependiendo del tipo de Plex. Los objetos de controlador pueden administrar la entrada/salida de datos para cualquier número de objetos de LUN.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> </dl>

 

 
