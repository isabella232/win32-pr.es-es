---
description: Los proveedores de hardware implementan las interfaces IVssProviderCreateSnapshotSet e IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Desarrollo de proveedores de hardware de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29533838b814a07f3da5310302a283f6cd60dc75779b4eb29dcdbf6b10816aa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032715"
---
# <a name="developing-vss-hardware-providers"></a>Desarrollo de proveedores de hardware de VSS

Los proveedores de hardware implementan [**las interfaces IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) [**e IVssHardwareSnapshotProvider.**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) **IVssProviderCreateSnapshotSet** implementa la secuenciación de estado de instantánea. **IVssHardwareSnapshotProvider** funciona en una abstracción lun. Los proveedores deben implementarse como un servidor COM fuera de proceso. Los proveedores usan mecanismos específicos del proveedor (a menudo IOCTL privados) para comunicarse con el subsistema de almacenamiento que crea instancias de los LUN de instantáneas.

-   [Registro y carga del proveedor de instantáneas](shadow-copy-provider-registration-and-loading.md)
-   [Creación de instantáneas para proveedores](shadow-copy-creation-for-providers.md)
-   [Interacciones y comportamientos del proveedor de hardware](hardware-provider-interactions-and-behaviors.md)

 

 



