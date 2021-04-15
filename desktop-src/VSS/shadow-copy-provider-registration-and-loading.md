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
# <a name="shadow-copy-provider-registration-and-loading"></a><span data-ttu-id="1755f-103">Registro y carga del proveedor de instantáneas</span><span class="sxs-lookup"><span data-stu-id="1755f-103">Shadow Copy Provider Registration and Loading</span></span>

## <a name="provider-registration"></a><span data-ttu-id="1755f-104">Registro del proveedor</span><span class="sxs-lookup"><span data-stu-id="1755f-104">Provider Registration</span></span>

<span data-ttu-id="1755f-105">VSS solo llama a los proveedores.</span><span class="sxs-lookup"><span data-stu-id="1755f-105">Only VSS calls providers.</span></span> <span data-ttu-id="1755f-106">El proveedor se registra para las llamadas mediante la invocación de [**IVssAdmin:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), pasando el **\_ \_ hardware de VSS Prov** para el parámetro *eProviderType* .</span><span class="sxs-lookup"><span data-stu-id="1755f-106">The provider registers for calls by invoking [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passing **VSS\_PROV\_HARDWARE** for the *eProviderType* parameter.</span></span> <span data-ttu-id="1755f-107">Una vez registrado, el proveedor participará en la administración de instantáneas hasta que se anule el registro mediante [**IVssAdmin:: UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span><span class="sxs-lookup"><span data-stu-id="1755f-107">Once registered, the provider will be involved in shadow copy management until unregistering using [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span></span>

## <a name="provider-loading-and-unloading"></a><span data-ttu-id="1755f-108">Carga y descarga de proveedores</span><span class="sxs-lookup"><span data-stu-id="1755f-108">Provider Loading and Unloading</span></span>

<span data-ttu-id="1755f-109">Los proveedores se pueden cargar y descargar con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1755f-109">Providers can be frequently loaded and unloaded.</span></span> <span data-ttu-id="1755f-110">Los proveedores pueden implementar [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) para determinar el momento en que VSS carga o descarga el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1755f-110">Providers can implement [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) to determine when VSS is loading or unloading the provider.</span></span>

 

 



