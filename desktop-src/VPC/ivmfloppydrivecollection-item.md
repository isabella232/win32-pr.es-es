---
title: Propiedad del elemento IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Objeto de disquete que corresponde al índice especificado.
ms.assetid: 068a1f1c-ae84-4689-b68a-ce25b68fc06b
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMFloppyDriveCollection
- Interfaz IVMFloppyDriveCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Item
- IVMFloppyDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315eaea13699d78a75457f39c6c915b30fa2fa9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151080"
---
# <a name="ivmfloppydrivecollectionitem-property"></a><span data-ttu-id="565a8-106">IVMFloppyDriveCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="565a8-106">IVMFloppyDriveCollection::Item property</span></span>

<span data-ttu-id="565a8-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="565a8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="565a8-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="565a8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="565a8-109">Recupera el objeto de disquete que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="565a8-109">Retrieves the floppy object that corresponds to the specified index.</span></span>

<span data-ttu-id="565a8-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="565a8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="565a8-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="565a8-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long           index,
  [out, retval] IVMFloppyDrive **floppyDrive
);
```



## <a name="property-value"></a><span data-ttu-id="565a8-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="565a8-112">Property value</span></span>

<span data-ttu-id="565a8-113">El objeto [**IVMFloppyDrive**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="565a8-113">The [**IVMFloppyDrive**](ivmfloppydrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="565a8-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="565a8-114">Error codes</span></span>



| <span data-ttu-id="565a8-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="565a8-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="565a8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="565a8-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="565a8-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="565a8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="565a8-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="565a8-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="565a8-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="565a8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="565a8-120">El parámetro *floppyDrive* es **null**.</span><span class="sxs-lookup"><span data-stu-id="565a8-120">The *floppyDrive* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="565a8-121"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="565a8-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="565a8-122">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="565a8-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="565a8-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="565a8-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="565a8-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="565a8-124">The configuration is unknown.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="565a8-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="565a8-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="565a8-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="565a8-126">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="565a8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="565a8-127">Requirements</span></span>



| <span data-ttu-id="565a8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="565a8-128">Requirement</span></span> | <span data-ttu-id="565a8-129">Value</span><span class="sxs-lookup"><span data-stu-id="565a8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="565a8-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="565a8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="565a8-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="565a8-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="565a8-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="565a8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="565a8-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="565a8-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="565a8-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="565a8-134">End of client support</span></span><br/>    | <span data-ttu-id="565a8-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="565a8-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="565a8-136">Producto</span><span class="sxs-lookup"><span data-stu-id="565a8-136">Product</span></span><br/>                  | <span data-ttu-id="565a8-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="565a8-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="565a8-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="565a8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="565a8-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="565a8-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="565a8-140">IID</span><span class="sxs-lookup"><span data-stu-id="565a8-140">IID</span></span><br/>                      | <span data-ttu-id="565a8-141">IID \_ IVMFloppyDriveCollection se define como 8ba70a25-F698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="565a8-141">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="565a8-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="565a8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="565a8-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="565a8-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="565a8-144">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="565a8-144">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

