---
title: Propiedad IVMVirtualPC Tasks (VPCCOMInterfaces. h)
description: Recupera una colección de tareas.
ms.assetid: bba9c4b4-c933-43c8-9fbc-f2beb59867cf
keywords:
- Propiedades de tareas Virtual PC
- Propiedad Tasks Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad Tasks
topic_type:
- apiref
api_name:
- IVMVirtualPC.Tasks
- IVMVirtualPC.get_Tasks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83eb27a48654a52a5724768da4ecf38584ea1231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905468"
---
# <a name="ivmvirtualpctasks-property"></a><span data-ttu-id="b147e-106">IVMVirtualPC:: Tasks (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b147e-106">IVMVirtualPC::Tasks property</span></span>

<span data-ttu-id="b147e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b147e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b147e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b147e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b147e-109">Recupera una colección de tareas.</span><span class="sxs-lookup"><span data-stu-id="b147e-109">Retrieves a collection of tasks.</span></span>

<span data-ttu-id="b147e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b147e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b147e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b147e-111">Syntax</span></span>


```C++
HRESULT get_Tasks(
  [out, retval] IVMTaskCollection **taskCollection
);
```



## <a name="property-value"></a><span data-ttu-id="b147e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b147e-112">Property value</span></span>

<span data-ttu-id="b147e-113">Colección de objetos [**IVMTask**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="b147e-113">A collection of [**IVMTask**](ivmtask.md) objects.</span></span> <span data-ttu-id="b147e-114">Vea [**IVMTaskCollection**](ivmtaskcollection.md).</span><span class="sxs-lookup"><span data-stu-id="b147e-114">See [**IVMTaskCollection**](ivmtaskcollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="b147e-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b147e-115">Error codes</span></span>



| <span data-ttu-id="b147e-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b147e-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="b147e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b147e-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b147e-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b147e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="b147e-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b147e-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b147e-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b147e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="b147e-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b147e-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="b147e-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b147e-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="b147e-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b147e-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="b147e-124"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="b147e-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="b147e-125">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="b147e-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b147e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b147e-126">Requirements</span></span>



| <span data-ttu-id="b147e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b147e-127">Requirement</span></span> | <span data-ttu-id="b147e-128">Value</span><span class="sxs-lookup"><span data-stu-id="b147e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b147e-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b147e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b147e-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b147e-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b147e-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b147e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b147e-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b147e-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b147e-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b147e-133">End of client support</span></span><br/>    | <span data-ttu-id="b147e-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b147e-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b147e-135">Producto</span><span class="sxs-lookup"><span data-stu-id="b147e-135">Product</span></span><br/>                  | <span data-ttu-id="b147e-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b147e-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b147e-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b147e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b147e-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b147e-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b147e-139">IID</span><span class="sxs-lookup"><span data-stu-id="b147e-139">IID</span></span><br/>                      | <span data-ttu-id="b147e-140">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="b147e-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b147e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b147e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b147e-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="b147e-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

