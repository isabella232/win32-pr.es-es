---
title: Método IVMVirtualMachineEvents OnGuestLogoff (VPCCOMInterfaces. h)
description: Recibe la notificación de que un usuario ha cerrado la sesión del sistema operativo invitado.
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- Método OnGuestLogoff Virtual PC
- Método OnGuestLogoff Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnGuestLogoff
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce5100c3901b3de32a769b6bae0e16fcffe26a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995892"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a><span data-ttu-id="f0330-106">IVMVirtualMachineEvents:: OnGuestLogoff (método)</span><span class="sxs-lookup"><span data-stu-id="f0330-106">IVMVirtualMachineEvents::OnGuestLogoff method</span></span>

<span data-ttu-id="f0330-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0330-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f0330-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0330-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f0330-109">Recibe la notificación de que un usuario ha cerrado la sesión del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="f0330-109">Receives notification that a user has logged off from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0330-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0330-110">Syntax</span></span>


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a><span data-ttu-id="f0330-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0330-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0330-112">*logoffType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0330-112">*logoffType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0330-113">Valor de la enumeración [**VMLogoffType**](vmlogofftype.md) que describe el tipo de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="f0330-113">Value from the [**VMLogoffType**](vmlogofftype.md) enumeration that describes the type of logoff.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0330-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0330-114">Return value</span></span>

<span data-ttu-id="f0330-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f0330-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0330-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0330-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0330-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0330-117">Requirements</span></span>



| <span data-ttu-id="f0330-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0330-118">Requirement</span></span> | <span data-ttu-id="f0330-119">Value</span><span class="sxs-lookup"><span data-stu-id="f0330-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0330-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0330-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0330-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0330-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0330-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0330-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0330-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0330-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f0330-124">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f0330-124">End of client support</span></span><br/>    | <span data-ttu-id="f0330-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0330-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f0330-126">Producto</span><span class="sxs-lookup"><span data-stu-id="f0330-126">Product</span></span><br/>                  | <span data-ttu-id="f0330-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f0330-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f0330-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0330-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0330-129"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0330-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f0330-130">IID</span><span class="sxs-lookup"><span data-stu-id="f0330-130">IID</span></span><br/>                      | <span data-ttu-id="f0330-131">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="f0330-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f0330-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0330-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0330-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="f0330-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> <dt>

[<span data-ttu-id="f0330-134">**VMLogoffType**</span><span class="sxs-lookup"><span data-stu-id="f0330-134">**VMLogoffType**</span></span>](vmlogofftype.md)
</dt> </dl>

 

