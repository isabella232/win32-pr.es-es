---
title: Propiedad de tiempo de actividad de IVMAccountant (VPCCOMInterfaces. h)
description: Recupera el número de segundos que se ha estado ejecutando la máquina virtual.
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- Propiedad de tiempo de actividad Virtual PC
- Propiedad de tiempo de actividad Virtual PC, interfaz IVMAccountant
- Interfaz IVMAccountant Virtual PC, propiedad de tiempo de actividad
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c496aa9c32d402dcc8e84bad5410ec7774d2a80a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150385"
---
# <a name="ivmaccountantuptime-property"></a><span data-ttu-id="9076e-106">IVMAccountant:: tiempo de actividad (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9076e-106">IVMAccountant::UpTime property</span></span>

<span data-ttu-id="9076e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9076e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9076e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9076e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9076e-109">Recupera el número de segundos que se ha estado ejecutando la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9076e-109">Retrieves the number of seconds that the virtual machine has been running.</span></span>

<span data-ttu-id="9076e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9076e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9076e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9076e-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="9076e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9076e-112">Property value</span></span>

<span data-ttu-id="9076e-113">número de segundos.</span><span class="sxs-lookup"><span data-stu-id="9076e-113">The number of seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9076e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9076e-114">Error codes</span></span>



| <span data-ttu-id="9076e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="9076e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="9076e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9076e-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9076e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9076e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9076e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9076e-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="9076e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9076e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="9076e-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="9076e-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="9076e-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9076e-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="9076e-122">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="9076e-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="9076e-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9076e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="9076e-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="9076e-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="9076e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9076e-125">Requirements</span></span>



| <span data-ttu-id="9076e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9076e-126">Requirement</span></span> | <span data-ttu-id="9076e-127">Value</span><span class="sxs-lookup"><span data-stu-id="9076e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9076e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9076e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9076e-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9076e-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9076e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9076e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9076e-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9076e-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9076e-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9076e-132">End of client support</span></span><br/>    | <span data-ttu-id="9076e-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9076e-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9076e-134">Producto</span><span class="sxs-lookup"><span data-stu-id="9076e-134">Product</span></span><br/>                  | <span data-ttu-id="9076e-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9076e-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9076e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9076e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9076e-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9076e-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9076e-138">IID</span><span class="sxs-lookup"><span data-stu-id="9076e-138">IID</span></span><br/>                      | <span data-ttu-id="9076e-139">IID \_ IVMAccountant se define como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="9076e-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="9076e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9076e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9076e-141">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="9076e-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

