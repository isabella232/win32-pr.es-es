---
title: Propiedad de recuento de IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera el número de unidades de CD y DVD de esta colección.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMDVDDriveCollection
- Interfaz IVMDVDDriveCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695965"
---
# <a name="ivmdvddrivecollectioncount-property"></a><span data-ttu-id="018ed-106">IVMDVDDriveCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="018ed-106">IVMDVDDriveCollection::Count property</span></span>

<span data-ttu-id="018ed-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="018ed-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="018ed-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="018ed-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="018ed-109">Recupera el número de unidades de CD y DVD de esta colección.</span><span class="sxs-lookup"><span data-stu-id="018ed-109">Retrieves the number of CD and DVD drives in this collection.</span></span>

<span data-ttu-id="018ed-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="018ed-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="018ed-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="018ed-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="018ed-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="018ed-112">Property value</span></span>

<span data-ttu-id="018ed-113">El número de unidades de CD y DVD.</span><span class="sxs-lookup"><span data-stu-id="018ed-113">The number of CD and DVD drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="018ed-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="018ed-114">Error codes</span></span>



| <span data-ttu-id="018ed-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="018ed-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="018ed-116">Significado</span><span class="sxs-lookup"><span data-stu-id="018ed-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="018ed-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="018ed-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="018ed-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="018ed-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="018ed-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="018ed-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="018ed-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="018ed-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="018ed-121"><dt>E \_ ERROR</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="018ed-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="018ed-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="018ed-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="018ed-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="018ed-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="018ed-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="018ed-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="018ed-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="018ed-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="018ed-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="018ed-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="018ed-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="018ed-127">Requirements</span></span>



| <span data-ttu-id="018ed-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="018ed-128">Requirement</span></span> | <span data-ttu-id="018ed-129">Value</span><span class="sxs-lookup"><span data-stu-id="018ed-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="018ed-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="018ed-130">Minimum supported client</span></span><br/> | <span data-ttu-id="018ed-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="018ed-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="018ed-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="018ed-132">Minimum supported server</span></span><br/> | <span data-ttu-id="018ed-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="018ed-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="018ed-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="018ed-134">End of client support</span></span><br/>    | <span data-ttu-id="018ed-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="018ed-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="018ed-136">Producto</span><span class="sxs-lookup"><span data-stu-id="018ed-136">Product</span></span><br/>                  | <span data-ttu-id="018ed-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="018ed-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="018ed-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="018ed-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="018ed-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="018ed-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="018ed-140">IID</span><span class="sxs-lookup"><span data-stu-id="018ed-140">IID</span></span><br/>                      | <span data-ttu-id="018ed-141">IID \_ IVMDVDDriveCollection se define como bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="018ed-141">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="018ed-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="018ed-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018ed-143">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="018ed-143">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

