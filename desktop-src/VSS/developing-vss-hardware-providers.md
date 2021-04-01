---
description: Los proveedores de hardware implementan las interfaces IVssProviderCreateSnapshotSet y IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Desarrollar proveedores de hardware de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279129"
---
# <a name="developing-vss-hardware-providers"></a>Desarrollar proveedores de hardware de VSS

Los proveedores de hardware implementan las interfaces [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) y [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) . **IVssProviderCreateSnapshotSet** implementa la secuencia de estado de la instantánea. **IVssHardwareSnapshotProvider** funciona en una abstracción de LUN. Los proveedores deben implementarse como un servidor COM fuera de proceso. Los proveedores usan mecanismos específicos del proveedor (a menudo, los ioctl privados) para comunicarse con el subsistema de almacenamiento que crea instancias de los LUN de instantáneas.

-   [Registro y carga del proveedor de instantáneas](shadow-copy-provider-registration-and-loading.md)
-   [Creación de instantáneas para proveedores](shadow-copy-creation-for-providers.md)
-   [Interacciones y comportamientos del proveedor de hardware](hardware-provider-interactions-and-behaviors.md)

 

 



