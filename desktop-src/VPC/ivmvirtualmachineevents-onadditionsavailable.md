---
title: Método IVMVirtualMachineEvents OnAdditionsAvailable (VPCCOMInterfaces. h)
description: Recibe una notificación de que los componentes de integración están disponibles en una máquina virtual.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- Método OnAdditionsAvailable Virtual PC
- Método OnAdditionsAvailable Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnAdditionsAvailable
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193b44f533079bc957cbb8b297409641814b6e21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492563"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a><span data-ttu-id="5f628-106">IVMVirtualMachineEvents:: OnAdditionsAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="5f628-106">IVMVirtualMachineEvents::OnAdditionsAvailable method</span></span>

<span data-ttu-id="5f628-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f628-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5f628-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5f628-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5f628-109">Recibe una notificación de que los componentes de integración están disponibles en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5f628-109">Receives notification that integration components are available in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f628-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f628-110">Syntax</span></span>


```C++
HRESULT OnAdditionsAvailable();
```



## <a name="parameters"></a><span data-ttu-id="5f628-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f628-111">Parameters</span></span>

<span data-ttu-id="5f628-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5f628-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f628-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f628-113">Return value</span></span>

<span data-ttu-id="5f628-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5f628-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f628-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f628-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f628-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f628-116">Requirements</span></span>



| <span data-ttu-id="5f628-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f628-117">Requirement</span></span> | <span data-ttu-id="5f628-118">Value</span><span class="sxs-lookup"><span data-stu-id="5f628-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f628-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f628-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f628-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f628-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f628-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f628-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f628-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5f628-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5f628-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5f628-123">End of client support</span></span><br/>    | <span data-ttu-id="5f628-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f628-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5f628-125">Producto</span><span class="sxs-lookup"><span data-stu-id="5f628-125">Product</span></span><br/>                  | <span data-ttu-id="5f628-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5f628-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5f628-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f628-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f628-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f628-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5f628-129">IID</span><span class="sxs-lookup"><span data-stu-id="5f628-129">IID</span></span><br/>                      | <span data-ttu-id="5f628-130">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="5f628-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="5f628-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f628-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f628-132">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="5f628-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

