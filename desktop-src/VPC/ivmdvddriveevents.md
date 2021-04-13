---
title: Interfaz IVMDVDDriveEvents (VPCCOMInterfaces. h)
description: Define la interfaz de eventos salientes para la interfaz IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Interfaz IVMDVDDriveEvents Virtual PC
- Interfaz IVMDVDDriveEvents Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492904"
---
# <a name="ivmdvddriveevents-interface"></a><span data-ttu-id="4ae1d-105">Interfaz IVMDVDDriveEvents</span><span class="sxs-lookup"><span data-stu-id="4ae1d-105">IVMDVDDriveEvents interface</span></span>

<span data-ttu-id="4ae1d-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4ae1d-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4ae1d-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4ae1d-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4ae1d-108">Define la interfaz de eventos salientes para la interfaz [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="4ae1d-108">Defines the outgoing event interface for the [**IVMDVDDrive**](ivmdvddrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4ae1d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4ae1d-109">Members</span></span>

<span data-ttu-id="4ae1d-110">La interfaz **IVMDVDDriveEvents** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4ae1d-110">The **IVMDVDDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4ae1d-111">**IVMDVDDriveEvents** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4ae1d-111">**IVMDVDDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="4ae1d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4ae1d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4ae1d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4ae1d-113">Methods</span></span>

<span data-ttu-id="4ae1d-114">La interfaz **IVMDVDDriveEvents** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4ae1d-114">The **IVMDVDDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="4ae1d-115">Método</span><span class="sxs-lookup"><span data-stu-id="4ae1d-115">Method</span></span>                                                   | <span data-ttu-id="4ae1d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ae1d-116">Description</span></span>                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="4ae1d-117">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="4ae1d-117">**OnMediaEject**</span></span>](ivmdvddriveevents-onmediaeject.md)   | <span data-ttu-id="4ae1d-118">Recibe la notificación de que se ha expulsado el medio de la unidad.</span><span class="sxs-lookup"><span data-stu-id="4ae1d-118">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="4ae1d-119">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="4ae1d-119">**OnMediaInsert**</span></span>](ivmdvddriveevents-onmediainsert.md) | <span data-ttu-id="4ae1d-120">Recibe la notificación de que los medios se han insertado en la unidad.</span><span class="sxs-lookup"><span data-stu-id="4ae1d-120">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4ae1d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ae1d-121">Requirements</span></span>



| <span data-ttu-id="4ae1d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae1d-122">Requirement</span></span> | <span data-ttu-id="4ae1d-123">Value</span><span class="sxs-lookup"><span data-stu-id="4ae1d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae1d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ae1d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ae1d-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ae1d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ae1d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ae1d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ae1d-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4ae1d-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4ae1d-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4ae1d-128">End of client support</span></span><br/>    | <span data-ttu-id="4ae1d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ae1d-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4ae1d-130">Producto</span><span class="sxs-lookup"><span data-stu-id="4ae1d-130">Product</span></span><br/>                  | <span data-ttu-id="4ae1d-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4ae1d-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4ae1d-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ae1d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ae1d-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae1d-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4ae1d-134">IID</span><span class="sxs-lookup"><span data-stu-id="4ae1d-134">IID</span></span><br/>                      | <span data-ttu-id="4ae1d-135">DIID \_ IVMDVDDriveEvents se define como c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="4ae1d-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



 

