---
title: Propiedad IVMTask ErrorDescription (VPCCOMInterfaces. h)
description: Recupera la descripción de error localizada registrada para esta tarea.
ms.assetid: 85728775-14b6-4031-9ccd-4c4f8c410705
keywords:
- Propiedad ErrorDescription Virtual PC
- Propiedad ErrorDescription Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, propiedad ErrorDescription
topic_type:
- apiref
api_name:
- IVMTask.ErrorDescription
- IVMTask.get_ErrorDescription
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5c95eac383d8e071832fdbf7843c01345278c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803475"
---
# <a name="ivmtaskerrordescription-property"></a><span data-ttu-id="63299-106">IVMTask:: ErrorDescription (propiedad)</span><span class="sxs-lookup"><span data-stu-id="63299-106">IVMTask::ErrorDescription property</span></span>

<span data-ttu-id="63299-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63299-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63299-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63299-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63299-109">Recupera la descripción de error localizada registrada para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="63299-109">Retrieves the localized error description recorded for this task.</span></span>

<span data-ttu-id="63299-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="63299-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63299-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63299-111">Syntax</span></span>


```C++
HRESULT get_ErrorDescription(
  [out, retval] BSTR *outErrorDesc
);
```



## <a name="property-value"></a><span data-ttu-id="63299-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="63299-112">Property value</span></span>

<span data-ttu-id="63299-113">Descripción de error.</span><span class="sxs-lookup"><span data-stu-id="63299-113">The error description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63299-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="63299-114">Error codes</span></span>



| <span data-ttu-id="63299-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="63299-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="63299-116">Significado</span><span class="sxs-lookup"><span data-stu-id="63299-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="63299-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63299-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="63299-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="63299-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="63299-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="63299-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="63299-120">El valor del parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="63299-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="63299-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="63299-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="63299-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="63299-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="63299-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63299-123">Requirements</span></span>



| <span data-ttu-id="63299-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="63299-124">Requirement</span></span> | <span data-ttu-id="63299-125">Value</span><span class="sxs-lookup"><span data-stu-id="63299-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63299-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63299-126">Minimum supported client</span></span><br/> | <span data-ttu-id="63299-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="63299-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63299-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63299-128">Minimum supported server</span></span><br/> | <span data-ttu-id="63299-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="63299-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="63299-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="63299-130">End of client support</span></span><br/>    | <span data-ttu-id="63299-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63299-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="63299-132">Producto</span><span class="sxs-lookup"><span data-stu-id="63299-132">Product</span></span><br/>                  | <span data-ttu-id="63299-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63299-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="63299-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63299-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="63299-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="63299-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="63299-136">IID</span><span class="sxs-lookup"><span data-stu-id="63299-136">IID</span></span><br/>                      | <span data-ttu-id="63299-137">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="63299-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="63299-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="63299-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63299-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="63299-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

