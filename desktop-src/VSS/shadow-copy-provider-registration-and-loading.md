---
description: Registro y carga del proveedor de instantáneas
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registro y carga del proveedor de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbb239303884314375ec865e3862d6a65af7de27bd7351a74e92604d06876bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998115"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Registro y carga del proveedor de instantáneas

## <a name="provider-registration"></a>Registro del proveedor

Solo VSS llama a proveedores. El proveedor se registra para las llamadas mediante la invocación de [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), pasando **\_ \_ VSS PROV HARDWARE** para el *parámetro eProviderType.* Una vez registrado, el proveedor participará en la administración de instantáneas hasta que se anula el registro [**mediante IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Carga y descarga de proveedores

Los proveedores se pueden cargar y descargar con frecuencia. Los proveedores pueden [**implementar IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) para determinar cuándo VSS carga o descarga el proveedor.

 

 



