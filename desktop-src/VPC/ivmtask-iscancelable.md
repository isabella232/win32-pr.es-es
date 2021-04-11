---
title: Propiedad IVMTask IsCancelable (VPCCOMInterfaces. h)
description: Determina si la tarea se puede cancelar.
ms.assetid: abb8a29a-7f5b-45ba-ae79-d422dfb2f39d
keywords:
- Propiedad IsCancelable Virtual PC
- Propiedad IsCancelable Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, propiedad IsCancelable
topic_type:
- apiref
api_name:
- IVMTask.IsCancelable
- IVMTask.get_IsCancelable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd06db3fc338277d7551233b0d609ceae03f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150948"
---
# <a name="ivmtaskiscancelable-property"></a><span data-ttu-id="feff2-106">IVMTask:: IsCancelable (propiedad)</span><span class="sxs-lookup"><span data-stu-id="feff2-106">IVMTask::IsCancelable property</span></span>

<span data-ttu-id="feff2-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="feff2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="feff2-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="feff2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="feff2-109">Determina si la tarea se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="feff2-109">Determines whether the task can be canceled.</span></span>

<span data-ttu-id="feff2-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="feff2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="feff2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="feff2-111">Syntax</span></span>


```C++
HRESULT get_IsCancelable(
  [out, retval] VARIANT_BOOL *isCancelable
);
```



## <a name="property-value"></a><span data-ttu-id="feff2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="feff2-112">Property value</span></span>

<span data-ttu-id="feff2-113">**True** si la tarea se puede cancelar antes de la finalización y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="feff2-113">**TRUE** if the task can be canceled before completion and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="feff2-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="feff2-114">Error codes</span></span>



| <span data-ttu-id="feff2-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="feff2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="feff2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="feff2-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="feff2-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="feff2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="feff2-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="feff2-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="feff2-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="feff2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="feff2-120">El valor del parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="feff2-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="feff2-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="feff2-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="feff2-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="feff2-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="feff2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feff2-123">Requirements</span></span>



| <span data-ttu-id="feff2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="feff2-124">Requirement</span></span> | <span data-ttu-id="feff2-125">Value</span><span class="sxs-lookup"><span data-stu-id="feff2-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="feff2-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feff2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="feff2-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="feff2-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="feff2-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feff2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="feff2-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="feff2-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="feff2-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="feff2-130">End of client support</span></span><br/>    | <span data-ttu-id="feff2-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="feff2-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="feff2-132">Producto</span><span class="sxs-lookup"><span data-stu-id="feff2-132">Product</span></span><br/>                  | <span data-ttu-id="feff2-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="feff2-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="feff2-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="feff2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="feff2-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="feff2-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="feff2-136">IID</span><span class="sxs-lookup"><span data-stu-id="feff2-136">IID</span></span><br/>                      | <span data-ttu-id="feff2-137">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="feff2-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="feff2-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="feff2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feff2-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="feff2-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

