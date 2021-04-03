---
title: Enumeración VMVirtualPCEvent (VPCCOMInterfaces. h)
description: Especifica los eventos de Windows Virtual PC.
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- Enumeración de VMVirtualPCEvent Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de7ecb639d0b62165dec691d522bed8116670c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079760"
---
# <a name="vmvirtualpcevent-enumeration"></a><span data-ttu-id="a5b83-104">Enumeración VMVirtualPCEvent</span><span class="sxs-lookup"><span data-stu-id="a5b83-104">VMVirtualPCEvent enumeration</span></span>

<span data-ttu-id="a5b83-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a5b83-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a5b83-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a5b83-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a5b83-107">Especifica los eventos de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a5b83-107">Specifies the Windows Virtual PC events.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b83-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5b83-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a><span data-ttu-id="a5b83-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="a5b83-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a5b83-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent \_ VMStateChange**</span><span class="sxs-lookup"><span data-stu-id="a5b83-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent\_VMStateChange**</span></span>
</dt> <dd>

<span data-ttu-id="a5b83-111">El estado de una máquina virtual ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a5b83-111">A virtual machine's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="a5b83-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent \_ EventLogged**</span><span class="sxs-lookup"><span data-stu-id="a5b83-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent\_EventLogged**</span></span>
</dt> <dd>

<span data-ttu-id="a5b83-113">Virtual PC ha registrado un evento.</span><span class="sxs-lookup"><span data-stu-id="a5b83-113">Virtual PC has logged an event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5b83-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5b83-114">Requirements</span></span>



| <span data-ttu-id="a5b83-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5b83-115">Requirement</span></span> | <span data-ttu-id="a5b83-116">Value</span><span class="sxs-lookup"><span data-stu-id="a5b83-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b83-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5b83-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b83-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5b83-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5b83-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5b83-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b83-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a5b83-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a5b83-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a5b83-121">End of client support</span></span><br/>    | <span data-ttu-id="a5b83-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5b83-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a5b83-123">Producto</span><span class="sxs-lookup"><span data-stu-id="a5b83-123">Product</span></span><br/>                  | <span data-ttu-id="a5b83-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a5b83-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a5b83-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5b83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b83-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b83-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b83-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5b83-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b83-128">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="a5b83-128">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

