---
description: Subsystem (objeto)
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Subsystem (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104562904"
---
# <a name="subsystem-object"></a>Subsystem (objeto)

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de subsistema modela un subsistema de almacenamiento. Un subsistema es un alojamiento RAID o una tarjeta RAID PCI. Un solo equipo host se puede conectar a cualquier número de subsistemas. Cada subsistema lo administra exactamente un proveedor de hardware. En una configuración de SAN, la clase de subsistema representa un contenedor de almacenamiento de SAN.

Un subsistema puede contener cualquier número de controladores y unidades, y puede mostrar (sin máscara) cualquier número de LUN en el equipo en el que se ejecuta el proveedor de hardware. Los subsistemas de un extremo superior pueden desenmascarar los LUN en otros equipos de la red. Cada unidad de disco dentro de un subsistema está conectada a un bus y ocupa una ranura en el bus. Cada controlador de un subsistema tiene uno o más puertos de controlador.

En la ilustración siguiente se muestran los dispositivos físicos contenidos en un subsistema (no se muestran los LUN) y las relaciones entre ellos.

![Diagrama que muestra un subsistema que empieza por "puertos" a la izquierda, pasando a "controladores" y, a continuación, un "bus" con "ranuras" que conducen a "unidades" individuales.](images/vdssubsystem.png)

Las aplicaciones de VDS usan el método [**IVdsHwProvider:: QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) para consultar los subsistemas que pertenecen a un proveedor de hardware específico. Los llamadores pueden obtener un puntero a un subsistema específico seleccionando el objeto de subsistema deseado de la enumeración devuelta por el método **QuerySubSystems** . Con un objeto de subsistema, puede establecer el estado del subsistema, crear Lun, reemplazar unidades y consultar controladores, unidades y LUN.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades de objeto de subsistema incluyen el estado del subsistema, el estado y las marcas. un recuento de los controladores, ranuras y buses; y un valor de prioridad de recompilación.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                                         | [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).                                                                                          |
| Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0 | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) y [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Interfaces que puede exponer este objeto                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) y [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Enumeraciones asociadas                                                                   | [**VDS \_ \_ \_ Marca de subsistema**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) y [**\_ \_ \_ Estado del subsistema de VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Estructuras asociadas                                                                     | [**VDS \_ \_Subsistema \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) y [**la \_ \_ \_ notificación del subsistema VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
