---
description: Subsystem (objeto)
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Subsystem (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af9837da90497b07d133362c0a61549a63665f2c75d4c97b2d07369e4589fa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603159"
---
# <a name="subsystem-object"></a>Subsystem (objeto)

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de subsistema modela un subsistema de almacenamiento. Un subsistema es un gabinete RAID o una tarjeta PCI RAID. Un único equipo host se puede conectar a cualquier número de subsistemas. Cada subsistema lo administra exactamente un proveedor de hardware. En una configuración de SAN, la clase de subsistema representa un gabinete de almacenamiento SAN.

Un subsistema puede contener cualquier número de controladores y unidades, y puede mostrar (desenmascarar) cualquier número de LUN en el equipo en el que se ejecuta el proveedor de hardware. Los subsistemas de nivel superior pueden desenmascarar LUN en otros equipos de la red. Cada unidad de disco dentro de un subsistema está conectada a un bus y ocupa una ranura en el bus. Cada controlador dentro de un subsistema tiene uno o varios puertos de controlador.

En la ilustración siguiente se muestran los dispositivos físicos contenidos en un subsistema (no se muestran LUN) y las relaciones entre ellos.

![Diagrama que muestra un subsistema que comienza con "Puertos" a la izquierda, se mueve a "Controladores" y, a continuación, un "Bus" con "Ranuras" que conduce a unidades individuales.](images/vdssubsystem.png)

Las aplicaciones VDS usan [**el método IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) para consultar los subsistemas que pertenecen a un proveedor de hardware específico. Los llamadores pueden obtener un puntero a un subsistema específico seleccionando el objeto de subsistema deseado de la enumeración devuelta por el **método QuerySubSystems.** Con un objeto de subsistema, puede establecer el estado del subsistema, crear LUN, reemplazar unidades y consultar controladores, unidades y LUN.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto de subsistema incluyen el estado del subsistema, el estado y las marcas; un recuento de controladores, ranuras y bus. y una configuración de prioridad de recompilación.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                                         | [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).                                                                                          |
| Interfaces que siempre expone este objeto en proveedores de iSCSI VDS 1.1 y 2.0 | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) [**e IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Interfaces que puede exponer este objeto                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) e [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Enumeraciones asociadas                                                                   | [**VDS \_ SUB \_ SYSTEM \_ FLAG y**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) [**VDS SUB SYSTEM \_ \_ \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Estructuras asociadas                                                                     | [**VDS \_ SUB \_ SYSTEM \_ PROP y**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) [**VDS SUB SYSTEM \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
