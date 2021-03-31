---
title: Método IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces. h)
description: Recibe la notificación de que un disco necesario para una máquina virtual tiene poco espacio disponible.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Método OnDiskOutOfSpace Virtual PC
- Método OnDiskOutOfSpace Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnDiskOutOfSpace
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904975"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a><span data-ttu-id="a560f-106">IVMVirtualMachineEvents:: OnDiskOutOfSpace (método)</span><span class="sxs-lookup"><span data-stu-id="a560f-106">IVMVirtualMachineEvents::OnDiskOutOfSpace method</span></span>

<span data-ttu-id="a560f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a560f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a560f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a560f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a560f-109">Recibe la notificación de que un disco necesario para una máquina virtual (VM) tiene poco espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="a560f-109">Receives notification that a disk required for a virtual machine (VM) is low on free space.</span></span> <span data-ttu-id="a560f-110">Si el espacio libre cae por debajo de 100 MB, este evento se recibe como una advertencia y si el espacio disponible cae por debajo de 20 MB, este evento se vuelve a recibir como un error y se pausa la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a560f-110">If free space drops below 100 MB this event is received as a warning and if free space drops below 20 MB this event is received again as an error and the VM will be paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="a560f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a560f-111">Syntax</span></span>


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a><span data-ttu-id="a560f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a560f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a560f-113">*criticallyLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a560f-113">*criticallyLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a560f-114">Establézcalo en **Variant \_ true** si el disco tiene menos de 20 MB libres y en **Variant \_ false** si el espacio disponible es superior a 20 MB pero inferior a 100 MB.</span><span class="sxs-lookup"><span data-stu-id="a560f-114">Set to **VARIANT\_TRUE** if the disk has less than 20 MB free and to **VARIANT\_FALSE** if the free space is more than 20 MB but less than 100 MB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a560f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a560f-115">Return value</span></span>

<span data-ttu-id="a560f-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a560f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a560f-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a560f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a560f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a560f-118">Requirements</span></span>



| <span data-ttu-id="a560f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a560f-119">Requirement</span></span> | <span data-ttu-id="a560f-120">Value</span><span class="sxs-lookup"><span data-stu-id="a560f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a560f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a560f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a560f-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a560f-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a560f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a560f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a560f-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a560f-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a560f-125">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a560f-125">End of client support</span></span><br/>    | <span data-ttu-id="a560f-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a560f-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a560f-127">Producto</span><span class="sxs-lookup"><span data-stu-id="a560f-127">Product</span></span><br/>                  | <span data-ttu-id="a560f-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a560f-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a560f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a560f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a560f-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a560f-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a560f-131">IID</span><span class="sxs-lookup"><span data-stu-id="a560f-131">IID</span></span><br/>                      | <span data-ttu-id="a560f-132">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="a560f-132">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="a560f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a560f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a560f-134">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="a560f-134">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

