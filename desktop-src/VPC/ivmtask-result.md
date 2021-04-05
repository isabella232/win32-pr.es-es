---
title: Propiedad de resultado IVMTask (VPCCOMInterfaces. h)
description: Recupera el resultado de la tarea.
ms.assetid: 640279ef-94b8-4e8f-88f3-a97cec54c121
keywords:
- Propiedad de resultado Virtual PC
- Propiedad de resultado Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, propiedad result
topic_type:
- apiref
api_name:
- IVMTask.Result
- IVMTask.get_Result
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4dc36d1529633a850bc10e5c89e8c07147aea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996769"
---
# <a name="ivmtaskresult-property"></a><span data-ttu-id="b8ce9-106">IVMTask:: result (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b8ce9-106">IVMTask::Result property</span></span>

<span data-ttu-id="b8ce9-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b8ce9-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b8ce9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b8ce9-109">Recupera el resultado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-109">Retrieves the result of the task.</span></span>

<span data-ttu-id="b8ce9-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ce9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8ce9-111">Syntax</span></span>


```C++
HRESULT get_Result(
  [out, retval] VMTaskResult *result
);
```



## <a name="property-value"></a><span data-ttu-id="b8ce9-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b8ce9-112">Property value</span></span>

<span data-ttu-id="b8ce9-113">Resultado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-113">The result of the task.</span></span> <span data-ttu-id="b8ce9-114">Para obtener una lista de valores, vea [**VMTaskResult**](vmtaskresult.md).</span><span class="sxs-lookup"><span data-stu-id="b8ce9-114">For a list of values, see [**VMTaskResult**](vmtaskresult.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="b8ce9-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b8ce9-115">Error codes</span></span>



| <span data-ttu-id="b8ce9-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b8ce9-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b8ce9-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b8ce9-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b8ce9-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b8ce9-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b8ce9-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b8ce9-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b8ce9-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b8ce9-121">El valor del parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="b8ce9-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b8ce9-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b8ce9-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b8ce9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8ce9-124">Requirements</span></span>



| <span data-ttu-id="b8ce9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8ce9-125">Requirement</span></span> | <span data-ttu-id="b8ce9-126">Value</span><span class="sxs-lookup"><span data-stu-id="b8ce9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ce9-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8ce9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ce9-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8ce9-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8ce9-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8ce9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ce9-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b8ce9-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b8ce9-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b8ce9-131">End of client support</span></span><br/>    | <span data-ttu-id="b8ce9-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8ce9-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b8ce9-133">Producto</span><span class="sxs-lookup"><span data-stu-id="b8ce9-133">Product</span></span><br/>                  | <span data-ttu-id="b8ce9-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b8ce9-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b8ce9-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8ce9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ce9-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ce9-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b8ce9-137">IID</span><span class="sxs-lookup"><span data-stu-id="b8ce9-137">IID</span></span><br/>                      | <span data-ttu-id="b8ce9-138">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="b8ce9-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="b8ce9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8ce9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ce9-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="b8ce9-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

