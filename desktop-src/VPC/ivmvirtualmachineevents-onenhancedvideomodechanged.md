---
title: Método IVMVirtualMachineEvents OnEnhancedVideoModeChanged (VPCCOMInterfaces. h)
description: Recibe una notificación de que ha cambiado la compatibilidad de una máquina virtual con el modo de vídeo mejorado.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Método OnEnhancedVideoModeChanged Virtual PC
- Método OnEnhancedVideoModeChanged Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnEnhancedVideoModeChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488920"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a><span data-ttu-id="8e681-106">IVMVirtualMachineEvents:: OnEnhancedVideoModeChanged (método)</span><span class="sxs-lookup"><span data-stu-id="8e681-106">IVMVirtualMachineEvents::OnEnhancedVideoModeChanged method</span></span>

<span data-ttu-id="8e681-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8e681-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e681-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e681-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e681-109">Recibe una notificación de que ha cambiado la compatibilidad de una máquina virtual con el modo de vídeo mejorado.</span><span class="sxs-lookup"><span data-stu-id="8e681-109">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e681-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e681-110">Syntax</span></span>


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a><span data-ttu-id="8e681-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e681-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e681-112">*enhancedVideoMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e681-112">*enhancedVideoMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e681-113">Indica si el modo de vídeo mejorado está disponible.</span><span class="sxs-lookup"><span data-stu-id="8e681-113">Indicates whether enhanced video mode is available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e681-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e681-114">Return value</span></span>

<span data-ttu-id="8e681-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8e681-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e681-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e681-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e681-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e681-117">Requirements</span></span>



| <span data-ttu-id="8e681-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e681-118">Requirement</span></span> | <span data-ttu-id="8e681-119">Value</span><span class="sxs-lookup"><span data-stu-id="8e681-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e681-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e681-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e681-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e681-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e681-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e681-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e681-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8e681-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8e681-124">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8e681-124">End of client support</span></span><br/>    | <span data-ttu-id="8e681-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e681-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8e681-126">Producto</span><span class="sxs-lookup"><span data-stu-id="8e681-126">Product</span></span><br/>                  | <span data-ttu-id="8e681-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e681-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8e681-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e681-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e681-129"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e681-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8e681-130">IID</span><span class="sxs-lookup"><span data-stu-id="8e681-130">IID</span></span><br/>                      | <span data-ttu-id="8e681-131">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="8e681-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="8e681-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e681-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e681-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="8e681-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

