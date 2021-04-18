---
title: Método IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces. h)
description: Recibe la notificación de que se ha realizado una solicitud de cierre.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Método OnRequestShutdown Virtual PC
- Método OnRequestShutdown Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnRequestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491296"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a><span data-ttu-id="aa744-106">IVMVirtualMachineEvents:: OnRequestShutdown (método)</span><span class="sxs-lookup"><span data-stu-id="aa744-106">IVMVirtualMachineEvents::OnRequestShutdown method</span></span>

<span data-ttu-id="aa744-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa744-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aa744-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="aa744-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aa744-109">Recibe la notificación de que se ha realizado una solicitud de cierre.</span><span class="sxs-lookup"><span data-stu-id="aa744-109">Receives notification that a shutdown request has been made.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa744-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa744-110">Syntax</span></span>


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="aa744-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa744-111">Parameters</span></span>

<span data-ttu-id="aa744-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="aa744-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa744-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa744-113">Return value</span></span>

<span data-ttu-id="aa744-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="aa744-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aa744-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa744-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa744-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa744-116">Remarks</span></span>

<span data-ttu-id="aa744-117">Se llama a este método cada vez que la sesión de máquina virtual está a punto de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="aa744-117">This method is called whenever the virtual machine session is about to shut down.</span></span> <span data-ttu-id="aa744-118">El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **vmVirtualMachineEvent \_ RequestShutdown** que se origina desde [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="aa744-118">The client program must implement this interface method to receive notification of the **vmVirtualMachineEvent\_RequestShutdown** event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="aa744-119">Esta notificación de eventos solo se envía cuando la sesión de máquinas virtuales está a punto de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="aa744-119">This event notification is sent only when the virtual machines session is about to shut down.</span></span> <span data-ttu-id="aa744-120">Las rutinas de apagado del sistema operativo, como [**IVMGuestOS:: Shutdown**](ivmguestos-shutdown.md), no activan este evento directamente a menos que también intenten realizar un apagado de software del hardware virtual.</span><span class="sxs-lookup"><span data-stu-id="aa744-120">Operating system shutdown routines, such as [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md), do not fire this event directly unless they also attempt to perform a software power off of the virtual hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa744-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa744-121">Requirements</span></span>



| <span data-ttu-id="aa744-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa744-122">Requirement</span></span> | <span data-ttu-id="aa744-123">Value</span><span class="sxs-lookup"><span data-stu-id="aa744-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa744-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa744-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa744-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa744-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa744-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa744-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa744-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aa744-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aa744-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="aa744-128">End of client support</span></span><br/>    | <span data-ttu-id="aa744-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa744-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aa744-130">Producto</span><span class="sxs-lookup"><span data-stu-id="aa744-130">Product</span></span><br/>                  | <span data-ttu-id="aa744-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aa744-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aa744-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa744-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa744-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa744-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="aa744-134">IID</span><span class="sxs-lookup"><span data-stu-id="aa744-134">IID</span></span><br/>                      | <span data-ttu-id="aa744-135">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="aa744-135">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="aa744-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa744-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa744-137">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="aa744-137">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

