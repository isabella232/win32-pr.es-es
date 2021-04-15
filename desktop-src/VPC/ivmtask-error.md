---
title: Propiedad de error IVMTask (VPCCOMInterfaces. h)
description: Recupera el error registrado para esta tarea.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Propiedad error Virtual PC
- Propiedad error Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, propiedad error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695960"
---
# <a name="ivmtaskerror-property"></a><span data-ttu-id="5105c-106">IVMTask:: error (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5105c-106">IVMTask::Error property</span></span>

<span data-ttu-id="5105c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5105c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5105c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5105c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5105c-109">Recupera el error registrado para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="5105c-109">Retrieves the error recorded for this task.</span></span>

<span data-ttu-id="5105c-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5105c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5105c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5105c-111">Syntax</span></span>


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a><span data-ttu-id="5105c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5105c-112">Property value</span></span>

<span data-ttu-id="5105c-113">Error registrado.</span><span class="sxs-lookup"><span data-stu-id="5105c-113">The recorded error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5105c-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5105c-114">Error codes</span></span>

<span data-ttu-id="5105c-115">Las instancias de [**IVMTask**](ivmtask.md) devueltas por otras interfaces pueden devolver valores adicionales.</span><span class="sxs-lookup"><span data-stu-id="5105c-115">Instances of [**IVMTask**](ivmtask.md) returned by other interfaces may return additional values.</span></span> <span data-ttu-id="5105c-116">Para obtener más información, consulte la documentación de los métodos que devuelven una instancia de **IVMTask** .</span><span class="sxs-lookup"><span data-stu-id="5105c-116">For details, see the documentation of the methods that return a **IVMTask** instance.</span></span>



| <span data-ttu-id="5105c-117">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="5105c-117">Name/value</span></span>                                                                                                                                                                        | <span data-ttu-id="5105c-118">Significado</span><span class="sxs-lookup"><span data-stu-id="5105c-118">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="5105c-119"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5105c-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                           | <span data-ttu-id="5105c-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5105c-120">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="5105c-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5105c-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                             | <span data-ttu-id="5105c-122">El valor del parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="5105c-122">The parameter value is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="5105c-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5105c-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                     | <span data-ttu-id="5105c-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="5105c-124">An unexpected error has occurred.</span></span><br/>                          |
| <dl> <span data-ttu-id="5105c-125"><dt>Máquina virtual \_ E \_ VMVIRTUALPC \_ \_ versión anterior</dt> <dt>0xA0040952</dt></span><span class="sxs-lookup"><span data-stu-id="5105c-125"><dt>VM\_E\_VMVIRTUALPC\_OLDER\_VERSION</dt> <dt>0xA0040952</dt></span></span> </dl>     | <span data-ttu-id="5105c-126">Tanto Virtual PC 2007 como Windows Virtual PC están instalados.</span><span class="sxs-lookup"><span data-stu-id="5105c-126">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <dl> <span data-ttu-id="5105c-127"><dt>Máquina virtual \_ E \_ otro \_ \_ software de virtualización</dt> <dt>0xA0040953</dt></span><span class="sxs-lookup"><span data-stu-id="5105c-127"><dt>VM\_E\_OTHER\_VIRTUALIZATION\_SOFTWARE</dt> <dt>0xA0040953</dt></span></span> </dl> | <span data-ttu-id="5105c-128">Se instala otro software de virtualización.</span><span class="sxs-lookup"><span data-stu-id="5105c-128">Other virtualization software is installed.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="5105c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5105c-129">Requirements</span></span>



| <span data-ttu-id="5105c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5105c-130">Requirement</span></span> | <span data-ttu-id="5105c-131">Value</span><span class="sxs-lookup"><span data-stu-id="5105c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5105c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5105c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5105c-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5105c-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5105c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5105c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5105c-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5105c-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5105c-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5105c-136">End of client support</span></span><br/>    | <span data-ttu-id="5105c-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5105c-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5105c-138">Producto</span><span class="sxs-lookup"><span data-stu-id="5105c-138">Product</span></span><br/>                  | <span data-ttu-id="5105c-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5105c-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5105c-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5105c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5105c-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5105c-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5105c-142">IID</span><span class="sxs-lookup"><span data-stu-id="5105c-142">IID</span></span><br/>                      | <span data-ttu-id="5105c-143">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="5105c-143">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="5105c-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="5105c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5105c-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="5105c-145">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

