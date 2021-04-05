---
title: Propiedad IVMTask PercentCompleted (VPCCOMInterfaces. h)
description: Recupera el porcentaje de finalización de la tarea.
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- Propiedad PercentCompleted Virtual PC
- Propiedad PercentCompleted Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, propiedad PercentCompleted
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa820adbbde2fc68632da27a9b146bd0e8f40143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803470"
---
# <a name="ivmtaskpercentcompleted-property"></a><span data-ttu-id="63fe8-106">IVMTask::P propiedad ercentCompleted</span><span class="sxs-lookup"><span data-stu-id="63fe8-106">IVMTask::PercentCompleted property</span></span>

<span data-ttu-id="63fe8-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63fe8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63fe8-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63fe8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63fe8-109">Recupera el porcentaje de finalización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="63fe8-109">Retrieves the completion percentage of the task.</span></span>

<span data-ttu-id="63fe8-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="63fe8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63fe8-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63fe8-111">Syntax</span></span>


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a><span data-ttu-id="63fe8-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="63fe8-112">Property value</span></span>

<span data-ttu-id="63fe8-113">Porcentaje de finalización actual.</span><span class="sxs-lookup"><span data-stu-id="63fe8-113">The current completion percentage.</span></span> <span data-ttu-id="63fe8-114">El valor es un número comprendido entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="63fe8-114">The value is a number between 0 and 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63fe8-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="63fe8-115">Error codes</span></span>



| <span data-ttu-id="63fe8-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="63fe8-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="63fe8-117">Significado</span><span class="sxs-lookup"><span data-stu-id="63fe8-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="63fe8-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63fe8-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="63fe8-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="63fe8-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="63fe8-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="63fe8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="63fe8-121">El valor del parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="63fe8-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="63fe8-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="63fe8-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="63fe8-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="63fe8-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="63fe8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63fe8-124">Requirements</span></span>



| <span data-ttu-id="63fe8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="63fe8-125">Requirement</span></span> | <span data-ttu-id="63fe8-126">Value</span><span class="sxs-lookup"><span data-stu-id="63fe8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63fe8-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63fe8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="63fe8-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="63fe8-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63fe8-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63fe8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="63fe8-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="63fe8-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="63fe8-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="63fe8-131">End of client support</span></span><br/>    | <span data-ttu-id="63fe8-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63fe8-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="63fe8-133">Producto</span><span class="sxs-lookup"><span data-stu-id="63fe8-133">Product</span></span><br/>                  | <span data-ttu-id="63fe8-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63fe8-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="63fe8-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63fe8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="63fe8-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="63fe8-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="63fe8-137">IID</span><span class="sxs-lookup"><span data-stu-id="63fe8-137">IID</span></span><br/>                      | <span data-ttu-id="63fe8-138">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="63fe8-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="63fe8-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="63fe8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63fe8-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="63fe8-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

