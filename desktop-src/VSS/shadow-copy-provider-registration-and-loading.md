---
description: Registro y carga del proveedor de instantáneas
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registro y carga del proveedor de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360599"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Registro y carga del proveedor de instantáneas

## <a name="provider-registration"></a>Registro del proveedor

VSS solo llama a los proveedores. El proveedor se registra para las llamadas mediante la invocación de [**IVssAdmin:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), pasando el **\_ \_ hardware de VSS Prov** para el parámetro *eProviderType* . Una vez registrado, el proveedor participará en la administración de instantáneas hasta que se anule el registro mediante [**IVssAdmin:: UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Carga y descarga de proveedores

Los proveedores se pueden cargar y descargar con frecuencia. Los proveedores pueden implementar [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) para determinar el momento en que VSS carga o descarga el proveedor.

 

 



