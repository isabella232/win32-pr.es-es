---
title: Propiedad del elemento IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera el objeto de unidad de CD o DVD que corresponde al índice especificado.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMDVDDriveCollection
- Interfaz IVMDVDDriveCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc631ab6d4de3ab65071bf2b8692236f3ae03ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079332"
---
# <a name="ivmdvddrivecollectionitem-property"></a><span data-ttu-id="2f3c7-106">IVMDVDDriveCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2f3c7-106">IVMDVDDriveCollection::Item property</span></span>

<span data-ttu-id="2f3c7-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2f3c7-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2f3c7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2f3c7-109">Recupera el objeto de unidad de CD o DVD que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-109">Retrieves the CD or DVD drive object that corresponds to the specified index.</span></span>

<span data-ttu-id="2f3c7-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f3c7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f3c7-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a><span data-ttu-id="2f3c7-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2f3c7-112">Property value</span></span>

<span data-ttu-id="2f3c7-113">El objeto [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="2f3c7-113">The [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f3c7-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2f3c7-114">Error codes</span></span>



| <span data-ttu-id="2f3c7-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="2f3c7-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2f3c7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2f3c7-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f3c7-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2f3c7-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="2f3c7-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2f3c7-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-120">The parameter is **NULL**.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="2f3c7-121"><dt>E \_ ERROR</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c7-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="2f3c7-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-122">An unexpected error has occurred.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="2f3c7-123"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c7-123"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="2f3c7-124">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-124">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="2f3c7-125"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2f3c7-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="2f3c7-126">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-126">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="2f3c7-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c7-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2f3c7-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2f3c7-128">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="2f3c7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f3c7-129">Requirements</span></span>



| <span data-ttu-id="2f3c7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f3c7-130">Requirement</span></span> | <span data-ttu-id="2f3c7-131">Value</span><span class="sxs-lookup"><span data-stu-id="2f3c7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c7-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f3c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2f3c7-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f3c7-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f3c7-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f3c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2f3c7-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2f3c7-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2f3c7-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2f3c7-136">End of client support</span></span><br/>    | <span data-ttu-id="2f3c7-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f3c7-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2f3c7-138">Producto</span><span class="sxs-lookup"><span data-stu-id="2f3c7-138">Product</span></span><br/>                  | <span data-ttu-id="2f3c7-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2f3c7-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2f3c7-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f3c7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f3c7-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c7-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2f3c7-142">IID</span><span class="sxs-lookup"><span data-stu-id="2f3c7-142">IID</span></span><br/>                      | <span data-ttu-id="2f3c7-143">IID \_ IVMDVDDriveCollection se define como bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="2f3c7-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="2f3c7-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f3c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3c7-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="2f3c7-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="2f3c7-146">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="2f3c7-146">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

