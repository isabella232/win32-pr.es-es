---
title: Interfaz IVMVirtualPCEvents (VPCCOMInterfaces. h)
description: Define la interfaz de eventos salientes para la interfaz IVMVirtualPC.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Interfaz IVMVirtualPCEvents Virtual PC
- Interfaz IVMVirtualPCEvents Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079613"
---
# <a name="ivmvirtualpcevents-interface"></a><span data-ttu-id="bd2f3-105">Interfaz IVMVirtualPCEvents</span><span class="sxs-lookup"><span data-stu-id="bd2f3-105">IVMVirtualPCEvents interface</span></span>

<span data-ttu-id="bd2f3-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bd2f3-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bd2f3-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bd2f3-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bd2f3-108">Define la interfaz de eventos salientes para la interfaz [**IVMVirtualPC**](ivmvirtualpc.md) .</span><span class="sxs-lookup"><span data-stu-id="bd2f3-108">Defines the outgoing event interface for the [**IVMVirtualPC**](ivmvirtualpc.md) interface.</span></span> <span data-ttu-id="bd2f3-109">El cliente implementa estos métodos para recibir los eventos enviados desde [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="bd2f3-109">The client implements these methods to receive events sent from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="members"></a><span data-ttu-id="bd2f3-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="bd2f3-110">Members</span></span>

<span data-ttu-id="bd2f3-111">La interfaz **IVMVirtualPCEvents** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="bd2f3-111">The **IVMVirtualPCEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="bd2f3-112">**IVMVirtualPCEvents** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bd2f3-112">**IVMVirtualPCEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="bd2f3-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="bd2f3-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bd2f3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="bd2f3-114">Methods</span></span>

<span data-ttu-id="bd2f3-115">La interfaz **IVMVirtualPCEvents** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bd2f3-115">The **IVMVirtualPCEvents** interface has these methods.</span></span>



| <span data-ttu-id="bd2f3-116">Método</span><span class="sxs-lookup"><span data-stu-id="bd2f3-116">Method</span></span>                                                        | <span data-ttu-id="bd2f3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd2f3-117">Description</span></span>                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="bd2f3-118">**OnEventLogged**</span><span class="sxs-lookup"><span data-stu-id="bd2f3-118">**OnEventLogged**</span></span>](ivmvirtualpcevents-oneventlogged.md)     | <span data-ttu-id="bd2f3-119">Recibe la notificación de que Windows Virtual PC registra un evento.</span><span class="sxs-lookup"><span data-stu-id="bd2f3-119">Receives notification that Windows Virtual PC logs an event.</span></span><br/>      |
| [<span data-ttu-id="bd2f3-120">**OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="bd2f3-120">**OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md) | <span data-ttu-id="bd2f3-121">Recibe la notificación de que el estado de una máquina virtual ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="bd2f3-121">Receives notification that a virtual machine's state has changed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd2f3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd2f3-122">Requirements</span></span>



| <span data-ttu-id="bd2f3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd2f3-123">Requirement</span></span> | <span data-ttu-id="bd2f3-124">Value</span><span class="sxs-lookup"><span data-stu-id="bd2f3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2f3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd2f3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2f3-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd2f3-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd2f3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd2f3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2f3-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bd2f3-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bd2f3-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bd2f3-129">End of client support</span></span><br/>    | <span data-ttu-id="bd2f3-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd2f3-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bd2f3-131">Producto</span><span class="sxs-lookup"><span data-stu-id="bd2f3-131">Product</span></span><br/>                  | <span data-ttu-id="bd2f3-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bd2f3-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bd2f3-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd2f3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd2f3-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd2f3-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bd2f3-135">IID</span><span class="sxs-lookup"><span data-stu-id="bd2f3-135">IID</span></span><br/>                      | <span data-ttu-id="bd2f3-136">DIID \_ IVMVirtualPCEvents se define como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="bd2f3-136">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



 

