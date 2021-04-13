---
title: Método IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
description: Recibe la notificación de que el estado de una máquina virtual ha cambiado. | Método IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Método OnStateChange Virtual PC
- Método OnStateChange Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnStateChange
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362363"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a><span data-ttu-id="30af7-107">IVMVirtualMachineEvents:: OnStateChange (método)</span><span class="sxs-lookup"><span data-stu-id="30af7-107">IVMVirtualMachineEvents::OnStateChange method</span></span>

<span data-ttu-id="30af7-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="30af7-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="30af7-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="30af7-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="30af7-110">Recibe la notificación de que el estado de una máquina virtual ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="30af7-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="30af7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30af7-111">Syntax</span></span>


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="30af7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30af7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30af7-113">*virtualMachineState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30af7-113">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30af7-114">El nuevo estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="30af7-114">The new state of the virtual machine.</span></span> <span data-ttu-id="30af7-115">Para obtener una lista de valores, vea [**VMVMState**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="30af7-115">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30af7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30af7-116">Return value</span></span>

<span data-ttu-id="30af7-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="30af7-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30af7-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30af7-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30af7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30af7-119">Remarks</span></span>

<span data-ttu-id="30af7-120">Se llama a este método cuando cambia el estado de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="30af7-120">This method is called when the state for this virtual machine changes.</span></span> <span data-ttu-id="30af7-121">El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmVirtualMachineEvent StateChanged que se origina desde [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="30af7-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_StateChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30af7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30af7-122">Requirements</span></span>



| <span data-ttu-id="30af7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="30af7-123">Requirement</span></span> | <span data-ttu-id="30af7-124">Value</span><span class="sxs-lookup"><span data-stu-id="30af7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="30af7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30af7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="30af7-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="30af7-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30af7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30af7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="30af7-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="30af7-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="30af7-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="30af7-129">End of client support</span></span><br/>    | <span data-ttu-id="30af7-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30af7-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="30af7-131">Producto</span><span class="sxs-lookup"><span data-stu-id="30af7-131">Product</span></span><br/>                  | <span data-ttu-id="30af7-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="30af7-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="30af7-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30af7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="30af7-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="30af7-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="30af7-135">IID</span><span class="sxs-lookup"><span data-stu-id="30af7-135">IID</span></span><br/>                      | <span data-ttu-id="30af7-136">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="30af7-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="30af7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="30af7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30af7-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="30af7-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

