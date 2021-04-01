---
title: Propiedad IVMDVDDrive ImageFile (VPCCOMInterfaces. h)
description: Recupera la ruta de acceso completa del conjunto de archivos de imagen para este dispositivo.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- ImageFile (propiedad, equipo virtual)
- ImageFile (propiedad, Virtual PC, interfaz IVMDVDDrive)
- Interfaz IVMDVDDrive Virtual PC, propiedad ImageFile
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905560"
---
# <a name="ivmdvddriveimagefile-property"></a><span data-ttu-id="fbc91-106">IVMDVDDrive:: ImageFile (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fbc91-106">IVMDVDDrive::ImageFile property</span></span>

<span data-ttu-id="fbc91-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fbc91-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fbc91-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fbc91-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fbc91-109">Recupera la ruta de acceso completa del conjunto de archivos de imagen para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbc91-109">Retrieves the full path of the image file set for this device.</span></span>

<span data-ttu-id="fbc91-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fbc91-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc91-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbc91-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a><span data-ttu-id="fbc91-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fbc91-112">Property value</span></span>

<span data-ttu-id="fbc91-113">Ruta de acceso completa al archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="fbc91-113">The full path to the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fbc91-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fbc91-114">Error codes</span></span>



| <span data-ttu-id="fbc91-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="fbc91-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="fbc91-116">Significado</span><span class="sxs-lookup"><span data-stu-id="fbc91-116">Meaning</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbc91-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fbc91-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="fbc91-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fbc91-118">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="fbc91-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fbc91-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="fbc91-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="fbc91-120">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="fbc91-121"><dt>E \_ ERROR</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="fbc91-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="fbc91-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="fbc91-122">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="fbc91-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fbc91-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="fbc91-124">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fbc91-124">The virtual machine could not be found.</span></span><br/>                        |
| <dl> <span data-ttu-id="fbc91-125"><dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fbc91-125"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="fbc91-126">La ubicación del bus para esta unidad no es válida.</span><span class="sxs-lookup"><span data-stu-id="fbc91-126">The bus location for this drive is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="fbc91-127"><dt>Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="fbc91-127"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="fbc91-128">El medio capturado por esta unidad de DVD no es un archivo de imagen ISO.</span><span class="sxs-lookup"><span data-stu-id="fbc91-128">The media captured by this DVD drive is not an ISO image file.</span></span><br/> |
| <dl> <span data-ttu-id="fbc91-129"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fbc91-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="fbc91-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="fbc91-130">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="fbc91-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbc91-131">Requirements</span></span>



| <span data-ttu-id="fbc91-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbc91-132">Requirement</span></span> | <span data-ttu-id="fbc91-133">Value</span><span class="sxs-lookup"><span data-stu-id="fbc91-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc91-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbc91-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc91-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbc91-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbc91-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbc91-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc91-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fbc91-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fbc91-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fbc91-138">End of client support</span></span><br/>    | <span data-ttu-id="fbc91-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbc91-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fbc91-140">Producto</span><span class="sxs-lookup"><span data-stu-id="fbc91-140">Product</span></span><br/>                  | <span data-ttu-id="fbc91-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fbc91-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fbc91-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbc91-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc91-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc91-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fbc91-144">IID</span><span class="sxs-lookup"><span data-stu-id="fbc91-144">IID</span></span><br/>                      | <span data-ttu-id="fbc91-145">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="fbc91-145">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="fbc91-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbc91-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc91-147">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="fbc91-147">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

