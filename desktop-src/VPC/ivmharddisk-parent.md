---
title: Propiedad primaria IVMHardDisk (VPCCOMInterfaces. h)
description: Primario del disco duro virtual de diferenciación.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Propiedad principal de PC virtual
- Propiedad primaria Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad principal
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995899"
---
# <a name="ivmharddiskparent-property"></a><span data-ttu-id="390f2-106">IVMHardDisk::P propiedad Princip</span><span class="sxs-lookup"><span data-stu-id="390f2-106">IVMHardDisk::Parent property</span></span>

<span data-ttu-id="390f2-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="390f2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="390f2-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="390f2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="390f2-109">Recupera y establece el elemento primario del disco duro virtual de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="390f2-109">Retrieves and sets the parent of the differencing virtual hard disk.</span></span>

<span data-ttu-id="390f2-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="390f2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="390f2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="390f2-111">Syntax</span></span>


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a><span data-ttu-id="390f2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="390f2-112">Property value</span></span>

<span data-ttu-id="390f2-113">Establece el objeto [**IVMHardDisk**](ivmharddisk.md) asociado a la imagen del disco duro principal.</span><span class="sxs-lookup"><span data-stu-id="390f2-113">Sets the [**IVMHardDisk**](ivmharddisk.md) object associated with the parent hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="390f2-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="390f2-114">Error codes</span></span>



| <span data-ttu-id="390f2-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="390f2-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="390f2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="390f2-116">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="390f2-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="390f2-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="390f2-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="390f2-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="390f2-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="390f2-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="390f2-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="390f2-122">No se trata de un disco duro de diferenciación, por lo que no tiene ningún elemento primario.</span><span class="sxs-lookup"><span data-stu-id="390f2-122">This is not a differencing hard disk, so it has no parent.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="390f2-123"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="390f2-124">El sistema no encontró el archivo del disco duro virtual principal.</span><span class="sxs-lookup"><span data-stu-id="390f2-124">The system could not find the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="390f2-125"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="390f2-126">El sistema no encontró la ruta de acceso al archivo de disco duro virtual principal.</span><span class="sxs-lookup"><span data-stu-id="390f2-126">The system could not find the path to the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="390f2-127"><dt>Máquina virtual \_ E \_ HD \_ Image \_ Open \_ FAIL</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-127"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="390f2-128">Se produjo un error al intentar abrir el archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="390f2-128">An error occurred while attempting to open the current hard disk image file.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="390f2-129"><dt>Máquina virtual \_ E 0xA0040681 de \_ \_ \_ acceso a imágenes HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="390f2-129"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="390f2-130">Error al intentar obtener acceso al archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="390f2-130">An error occurred while attempting to access the current hard disk image file.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="390f2-131"><dt>Máquina virtual \_ Error \_ de \_ \_ \_ coincidencia de ID. de elemento secundario E</dt> <dt>0xA0040685</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-131"><dt>VM\_E\_PARENT\_CHILD\_ID\_MISMATCH</dt> <dt>0xA0040685</dt></span></span> </dl>            | <span data-ttu-id="390f2-132">La imagen del disco duro virtual que se encuentra en el parámetro *primario* no tiene el mismo identificador que la imagen de disco secundaria.</span><span class="sxs-lookup"><span data-stu-id="390f2-132">The virtual hard disk image located by the *parent* parameter does not have the same ID as the child disk image.</span></span> <span data-ttu-id="390f2-133">Asegúrese de que la imagen del disco duro virtual principal que se encuentra en el parámetro *principal* es la misma que se usa para crear la imagen de disco duro virtual de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="390f2-133">Make sure the parent virtual hard disk image located by the *parent* parameter is the same image used to create the differencing virtual hard disk image.</span></span><br/> |
| <dl> <span data-ttu-id="390f2-134"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="390f2-135">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="390f2-135">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="390f2-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="390f2-136">Remarks</span></span>

<span data-ttu-id="390f2-137">Esta propiedad solo es válida con imágenes de disco duro de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="390f2-137">This property is only valid with differencing hard disk images.</span></span>

## <a name="requirements"></a><span data-ttu-id="390f2-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="390f2-138">Requirements</span></span>



| <span data-ttu-id="390f2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="390f2-139">Requirement</span></span> | <span data-ttu-id="390f2-140">Value</span><span class="sxs-lookup"><span data-stu-id="390f2-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="390f2-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="390f2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="390f2-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="390f2-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="390f2-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="390f2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="390f2-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="390f2-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="390f2-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="390f2-145">End of client support</span></span><br/>    | <span data-ttu-id="390f2-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="390f2-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="390f2-147">Producto</span><span class="sxs-lookup"><span data-stu-id="390f2-147">Product</span></span><br/>                  | <span data-ttu-id="390f2-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="390f2-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="390f2-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="390f2-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="390f2-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="390f2-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="390f2-151">IID</span><span class="sxs-lookup"><span data-stu-id="390f2-151">IID</span></span><br/>                      | <span data-ttu-id="390f2-152">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="390f2-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="390f2-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="390f2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390f2-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="390f2-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

