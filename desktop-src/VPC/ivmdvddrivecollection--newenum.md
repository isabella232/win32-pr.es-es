---
title: Propiedad _NewEnum IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera un enumerador para la colección de CD/DVD.
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- _NewEnum propiedad de PC virtual
- Propiedad _NewEnum Virtual PC, interfaz IVMDVDDriveCollection
- Interfaz IVMDVDDriveCollection Virtual PC, propiedad _NewEnum
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfd0de3aaf6b25808d1afa591b0c2099599e6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996344"
---
# <a name="ivmdvddrivecollection_newenum-property"></a><span data-ttu-id="2f691-106">IVMDVDDriveCollection:: \_ NewEnum (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2f691-106">IVMDVDDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="2f691-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f691-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2f691-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2f691-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2f691-109">Recupera un enumerador para la colección de CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="2f691-109">Retrieves an enumerator for the CD/DVD collection.</span></span>

<span data-ttu-id="2f691-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2f691-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f691-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f691-111">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="2f691-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2f691-112">Property value</span></span>

<span data-ttu-id="2f691-113">Enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="2f691-113">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f691-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2f691-114">Error codes</span></span>



| <span data-ttu-id="2f691-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="2f691-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2f691-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2f691-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2f691-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f691-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2f691-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2f691-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="2f691-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2f691-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2f691-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2f691-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="2f691-121"><dt>E \_ ERROR</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="2f691-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="2f691-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2f691-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="2f691-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2f691-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2f691-124">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2f691-124">An unexpected error occurred.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="2f691-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f691-125">Requirements</span></span>



| <span data-ttu-id="2f691-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f691-126">Requirement</span></span> | <span data-ttu-id="2f691-127">Value</span><span class="sxs-lookup"><span data-stu-id="2f691-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f691-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f691-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2f691-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f691-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f691-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f691-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2f691-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2f691-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2f691-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2f691-132">End of client support</span></span><br/>    | <span data-ttu-id="2f691-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f691-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2f691-134">Producto</span><span class="sxs-lookup"><span data-stu-id="2f691-134">Product</span></span><br/>                  | <span data-ttu-id="2f691-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2f691-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2f691-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f691-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f691-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f691-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2f691-138">IID</span><span class="sxs-lookup"><span data-stu-id="2f691-138">IID</span></span><br/>                      | <span data-ttu-id="2f691-139">IID \_ IVMDVDDriveCollection se define como bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="2f691-139">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="2f691-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f691-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f691-141">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="2f691-141">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

