---
title: Propiedad de identificador de IVMTask (VPCCOMInterfaces. h)
description: Recupera un identificador único para esta tarea.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- Propiedad ID Virtual PC
- Propiedad ID Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, propiedad ID
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905530"
---
# <a name="ivmtaskid-property"></a><span data-ttu-id="bf6ad-106">IVMTask:: ID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="bf6ad-106">IVMTask::ID property</span></span>

<span data-ttu-id="bf6ad-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bf6ad-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bf6ad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bf6ad-109">Recupera un identificador único para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-109">Retrieves a unique identifier for this task.</span></span>

<span data-ttu-id="bf6ad-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf6ad-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf6ad-111">Syntax</span></span>


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a><span data-ttu-id="bf6ad-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bf6ad-112">Property value</span></span>

<span data-ttu-id="bf6ad-113">El identificador único.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-113">The unique identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf6ad-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bf6ad-114">Error codes</span></span>



| <span data-ttu-id="bf6ad-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="bf6ad-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bf6ad-116">Significado</span><span class="sxs-lookup"><span data-stu-id="bf6ad-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bf6ad-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bf6ad-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bf6ad-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="bf6ad-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bf6ad-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bf6ad-120">El valor del parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="bf6ad-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bf6ad-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bf6ad-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="bf6ad-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bf6ad-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf6ad-123">Requirements</span></span>



| <span data-ttu-id="bf6ad-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf6ad-124">Requirement</span></span> | <span data-ttu-id="bf6ad-125">Value</span><span class="sxs-lookup"><span data-stu-id="bf6ad-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6ad-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf6ad-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bf6ad-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf6ad-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf6ad-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf6ad-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bf6ad-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bf6ad-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bf6ad-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bf6ad-130">End of client support</span></span><br/>    | <span data-ttu-id="bf6ad-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf6ad-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bf6ad-132">Producto</span><span class="sxs-lookup"><span data-stu-id="bf6ad-132">Product</span></span><br/>                  | <span data-ttu-id="bf6ad-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bf6ad-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bf6ad-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf6ad-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf6ad-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf6ad-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bf6ad-136">IID</span><span class="sxs-lookup"><span data-stu-id="bf6ad-136">IID</span></span><br/>                      | <span data-ttu-id="bf6ad-137">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="bf6ad-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="bf6ad-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf6ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf6ad-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="bf6ad-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

