---
title: Método IVMVirtualMachineEvents onreset (VPCCOMInterfaces. h)
description: Recibe la notificación de que una máquina virtual se ha restablecido.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- Método onreset Virtual PC
- Método onreset Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método onreset
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6345d0e925777fbecf42247b3e3064b9f993c7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995891"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a><span data-ttu-id="45b90-106">IVMVirtualMachineEvents:: onreset (método)</span><span class="sxs-lookup"><span data-stu-id="45b90-106">IVMVirtualMachineEvents::OnReset method</span></span>

<span data-ttu-id="45b90-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="45b90-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="45b90-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="45b90-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="45b90-109">Recibe la notificación de que una máquina virtual se ha restablecido.</span><span class="sxs-lookup"><span data-stu-id="45b90-109">Receives notification that a virtual machine has been reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b90-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45b90-110">Syntax</span></span>


```C++
HRESULT OnReset();
```



## <a name="parameters"></a><span data-ttu-id="45b90-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45b90-111">Parameters</span></span>

<span data-ttu-id="45b90-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="45b90-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45b90-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45b90-113">Return value</span></span>

<span data-ttu-id="45b90-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="45b90-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45b90-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45b90-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b90-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45b90-116">Remarks</span></span>

<span data-ttu-id="45b90-117">Se llama a este método cuando se ha restablecido la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="45b90-117">This method is called when the virtual machine has been reset.</span></span> <span data-ttu-id="45b90-118">El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento de restablecimiento de vmVirtualMachineEvent procedente de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="45b90-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_Reset event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45b90-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b90-119">Requirements</span></span>



| <span data-ttu-id="45b90-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b90-120">Requirement</span></span> | <span data-ttu-id="45b90-121">Value</span><span class="sxs-lookup"><span data-stu-id="45b90-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b90-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45b90-122">Minimum supported client</span></span><br/> | <span data-ttu-id="45b90-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="45b90-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45b90-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45b90-124">Minimum supported server</span></span><br/> | <span data-ttu-id="45b90-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="45b90-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="45b90-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="45b90-126">End of client support</span></span><br/>    | <span data-ttu-id="45b90-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45b90-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="45b90-128">Producto</span><span class="sxs-lookup"><span data-stu-id="45b90-128">Product</span></span><br/>                  | <span data-ttu-id="45b90-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="45b90-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="45b90-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45b90-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="45b90-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b90-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="45b90-132">IID</span><span class="sxs-lookup"><span data-stu-id="45b90-132">IID</span></span><br/>                      | <span data-ttu-id="45b90-133">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="45b90-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="45b90-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="45b90-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b90-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="45b90-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

