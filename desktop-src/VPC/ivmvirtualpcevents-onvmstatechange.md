---
title: Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
description: Recibe la notificación de que el estado de una máquina virtual ha cambiado. | Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Método OnVMStateChange Virtual PC
- Método OnVMStateChange Virtual PC, interfaz IVMVirtualPCEvents
- Interfaz IVMVirtualPCEvents Virtual PC, método OnVMStateChange
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698101"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a><span data-ttu-id="d25d7-107">IVMVirtualPCEvents:: OnVMStateChange (método)</span><span class="sxs-lookup"><span data-stu-id="d25d7-107">IVMVirtualPCEvents::OnVMStateChange method</span></span>

<span data-ttu-id="d25d7-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d25d7-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d25d7-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d25d7-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d25d7-110">Recibe la notificación de que el estado de una máquina virtual ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d25d7-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d25d7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d25d7-111">Syntax</span></span>


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="d25d7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d25d7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d25d7-113">*virtualMachineConfig* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d25d7-113">*virtualMachineConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d25d7-114">El nombre de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d25d7-114">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d25d7-115">*virtualMachineState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d25d7-115">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d25d7-116">El nuevo estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d25d7-116">The new state of the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d25d7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d25d7-117">Return value</span></span>

<span data-ttu-id="d25d7-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d25d7-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d25d7-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d25d7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d25d7-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d25d7-120">Remarks</span></span>

<span data-ttu-id="d25d7-121">El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **vmVirtualPCEvent \_ VMStateChanged** que se origina desde [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="d25d7-121">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_VMStateChanged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span> <span data-ttu-id="d25d7-122">Para supervisar una máquina virtual concreta, use el método [**IVMVirtualMachineEvents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="d25d7-122">To monitor a specific virtual machine, use the [**IVMVirtualMachineEvents::OnStateChange**](ivmvirtualmachineevents-onstatechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d25d7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d25d7-123">Requirements</span></span>



| <span data-ttu-id="d25d7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d25d7-124">Requirement</span></span> | <span data-ttu-id="d25d7-125">Value</span><span class="sxs-lookup"><span data-stu-id="d25d7-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d25d7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d25d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d25d7-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d25d7-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d25d7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d25d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d25d7-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d25d7-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d25d7-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d25d7-130">End of client support</span></span><br/>    | <span data-ttu-id="d25d7-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d25d7-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d25d7-132">Producto</span><span class="sxs-lookup"><span data-stu-id="d25d7-132">Product</span></span><br/>                  | <span data-ttu-id="d25d7-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d25d7-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d25d7-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d25d7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d25d7-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d25d7-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d25d7-136">IID</span><span class="sxs-lookup"><span data-stu-id="d25d7-136">IID</span></span><br/>                      | <span data-ttu-id="d25d7-137">DIID \_ IVMVirtualPCEvents se define como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="d25d7-137">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="d25d7-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d25d7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25d7-139">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="d25d7-139">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

