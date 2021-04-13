---
title: Método IVMVirtualMachineEvents OnGuestShutdown (VPCCOMInterfaces. h)
description: Recibe la notificación de cierre del sistema operativo invitado.
ms.assetid: a70c746a-f1ce-4f93-b41b-b03dc83f3da2
keywords:
- Método OnGuestShutdown Virtual PC
- Método OnGuestShutdown Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnGuestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481b6dd6e13dc17d7f9a22ef366e984c2663279c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534953"
---
# <a name="ivmvirtualmachineeventsonguestshutdown-method"></a><span data-ttu-id="beea1-106">IVMVirtualMachineEvents:: OnGuestShutdown (método)</span><span class="sxs-lookup"><span data-stu-id="beea1-106">IVMVirtualMachineEvents::OnGuestShutdown method</span></span>

<span data-ttu-id="beea1-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="beea1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="beea1-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="beea1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="beea1-109">Recibe la notificación de cierre del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="beea1-109">Receives notification that guest operating system shuts down.</span></span>

## <a name="syntax"></a><span data-ttu-id="beea1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="beea1-110">Syntax</span></span>


```C++
HRESULT OnGuestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="beea1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="beea1-111">Parameters</span></span>

<span data-ttu-id="beea1-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="beea1-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="beea1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beea1-113">Return value</span></span>

<span data-ttu-id="beea1-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="beea1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="beea1-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="beea1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="beea1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beea1-116">Requirements</span></span>



| <span data-ttu-id="beea1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="beea1-117">Requirement</span></span> | <span data-ttu-id="beea1-118">Value</span><span class="sxs-lookup"><span data-stu-id="beea1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="beea1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beea1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="beea1-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="beea1-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="beea1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beea1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="beea1-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="beea1-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="beea1-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="beea1-123">End of client support</span></span><br/>    | <span data-ttu-id="beea1-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="beea1-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="beea1-125">Producto</span><span class="sxs-lookup"><span data-stu-id="beea1-125">Product</span></span><br/>                  | <span data-ttu-id="beea1-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="beea1-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="beea1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="beea1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="beea1-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="beea1-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="beea1-129">IID</span><span class="sxs-lookup"><span data-stu-id="beea1-129">IID</span></span><br/>                      | <span data-ttu-id="beea1-130">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="beea1-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="beea1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="beea1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beea1-132">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="beea1-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

