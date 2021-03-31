---
title: Interfaz IVMFloppyDriveEvents (VPCCOMInterfaces. h)
description: Define la interfaz de eventos salientes para la interfaz IVMFloppyDrive. El cliente implementa estos métodos para recibir los eventos enviados desde IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Interfaz IVMFloppyDriveEvents Virtual PC
- Interfaz IVMFloppyDriveEvents Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151079"
---
# <a name="ivmfloppydriveevents-interface"></a><span data-ttu-id="6ab98-106">Interfaz IVMFloppyDriveEvents</span><span class="sxs-lookup"><span data-stu-id="6ab98-106">IVMFloppyDriveEvents interface</span></span>

<span data-ttu-id="6ab98-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6ab98-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6ab98-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6ab98-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6ab98-109">Define la interfaz de eventos salientes para la interfaz [**IVMFloppyDrive**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="6ab98-109">Defines the outgoing event interface for the [**IVMFloppyDrive**](ivmfloppydrive.md) interface.</span></span> <span data-ttu-id="6ab98-110">El cliente implementa estos métodos para recibir los eventos enviados desde **IVMFloppyDrive**.</span><span class="sxs-lookup"><span data-stu-id="6ab98-110">The client implements these methods to receive events sent from **IVMFloppyDrive**.</span></span>

## <a name="members"></a><span data-ttu-id="6ab98-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ab98-111">Members</span></span>

<span data-ttu-id="6ab98-112">La interfaz **IVMFloppyDriveEvents** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="6ab98-112">The **IVMFloppyDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6ab98-113">**IVMFloppyDriveEvents** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6ab98-113">**IVMFloppyDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="6ab98-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ab98-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6ab98-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ab98-115">Methods</span></span>

<span data-ttu-id="6ab98-116">La interfaz **IVMFloppyDriveEvents** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6ab98-116">The **IVMFloppyDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="6ab98-117">Método</span><span class="sxs-lookup"><span data-stu-id="6ab98-117">Method</span></span>                                                      | <span data-ttu-id="6ab98-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ab98-118">Description</span></span>                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="6ab98-119">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="6ab98-119">**OnMediaEject**</span></span>](ivmfloppydriveevents-onmediaeject.md)   | <span data-ttu-id="6ab98-120">Recibe la notificación de que se ha expulsado el medio de la unidad.</span><span class="sxs-lookup"><span data-stu-id="6ab98-120">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="6ab98-121">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="6ab98-121">**OnMediaInsert**</span></span>](ivmfloppydriveevents-onmediainsert.md) | <span data-ttu-id="6ab98-122">Recibe la notificación de que los medios se han insertado en la unidad.</span><span class="sxs-lookup"><span data-stu-id="6ab98-122">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6ab98-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ab98-123">Requirements</span></span>



| <span data-ttu-id="6ab98-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab98-124">Requirement</span></span> | <span data-ttu-id="6ab98-125">Value</span><span class="sxs-lookup"><span data-stu-id="6ab98-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab98-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ab98-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab98-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ab98-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ab98-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ab98-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab98-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6ab98-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6ab98-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6ab98-130">End of client support</span></span><br/>    | <span data-ttu-id="6ab98-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6ab98-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6ab98-132">Producto</span><span class="sxs-lookup"><span data-stu-id="6ab98-132">Product</span></span><br/>                  | <span data-ttu-id="6ab98-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6ab98-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6ab98-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ab98-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab98-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ab98-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6ab98-136">IID</span><span class="sxs-lookup"><span data-stu-id="6ab98-136">IID</span></span><br/>                      | <span data-ttu-id="6ab98-137">DIID \_ IVMFloppyDriveEvents se define como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="6ab98-137">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



 

