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
# <a name="developing-vss-hardware-providers"></a><span data-ttu-id="5d8a3-103">Desarrollar proveedores de hardware de VSS</span><span class="sxs-lookup"><span data-stu-id="5d8a3-103">Developing VSS Hardware Providers</span></span>

<span data-ttu-id="5d8a3-104">Los proveedores de hardware implementan las interfaces [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) y [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) .</span><span class="sxs-lookup"><span data-stu-id="5d8a3-104">Hardware providers implement the [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) and [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) interfaces.</span></span> <span data-ttu-id="5d8a3-105">**IVssProviderCreateSnapshotSet** implementa la secuencia de estado de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="5d8a3-105">**IVssProviderCreateSnapshotSet** implements the shadow copy state sequencing.</span></span> <span data-ttu-id="5d8a3-106">**IVssHardwareSnapshotProvider** funciona en una abstracción de LUN.</span><span class="sxs-lookup"><span data-stu-id="5d8a3-106">**IVssHardwareSnapshotProvider** operates on a LUN abstraction.</span></span> <span data-ttu-id="5d8a3-107">Los proveedores deben implementarse como un servidor COM fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="5d8a3-107">Providers must be implemented as an out-of-process COM server.</span></span> <span data-ttu-id="5d8a3-108">Los proveedores usan mecanismos específicos del proveedor (a menudo, los ioctl privados) para comunicarse con el subsistema de almacenamiento que crea instancias de los LUN de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="5d8a3-108">Providers use provider-specific mechanisms (often private IOCTLs) to communicate with the storage subsystem that instantiates the shadow copy LUNs.</span></span>

-   [<span data-ttu-id="5d8a3-109">Registro y carga del proveedor de instantáneas</span><span class="sxs-lookup"><span data-stu-id="5d8a3-109">Shadow Copy Provider Registration and Loading</span></span>](shadow-copy-provider-registration-and-loading.md)
-   [<span data-ttu-id="5d8a3-110">Creación de instantáneas para proveedores</span><span class="sxs-lookup"><span data-stu-id="5d8a3-110">Shadow Copy Creation for Providers</span></span>](shadow-copy-creation-for-providers.md)
-   [<span data-ttu-id="5d8a3-111">Interacciones y comportamientos del proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="5d8a3-111">Hardware Provider Interactions and Behaviors</span></span>](hardware-provider-interactions-and-behaviors.md)

 

 



