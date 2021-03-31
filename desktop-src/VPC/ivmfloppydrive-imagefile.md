---
title: Propiedad IVMFloppyDrive ImageFile (VPCCOMInterfaces. h)
description: Recupera la ruta de acceso completa del archivo de imagen al que está conectada la unidad de disquete.
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- ImageFile (propiedad, equipo virtual)
- ImageFile (propiedad, Virtual PC, interfaz IVMFloppyDrive)
- Interfaz IVMFloppyDrive Virtual PC, propiedad ImageFile
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa18c4a1da3137613e0106f828f59805e5615384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079584"
---
# <a name="ivmfloppydriveimagefile-property"></a><span data-ttu-id="29a0b-106">IVMFloppyDrive:: ImageFile (propiedad)</span><span class="sxs-lookup"><span data-stu-id="29a0b-106">IVMFloppyDrive::ImageFile property</span></span>

<span data-ttu-id="29a0b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="29a0b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="29a0b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="29a0b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="29a0b-109">Recupera la ruta de acceso completa del archivo de imagen al que está conectada la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="29a0b-109">Retrieves the full path of the image file to which the floppy drive is attached.</span></span>

<span data-ttu-id="29a0b-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="29a0b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a0b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29a0b-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a><span data-ttu-id="29a0b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="29a0b-112">Property value</span></span>

<span data-ttu-id="29a0b-113">Ruta de acceso completa del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="29a0b-113">The full path of the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="29a0b-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="29a0b-114">Error codes</span></span>



| <span data-ttu-id="29a0b-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="29a0b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="29a0b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="29a0b-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29a0b-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="29a0b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="29a0b-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="29a0b-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="29a0b-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="29a0b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="29a0b-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="29a0b-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="29a0b-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="29a0b-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="29a0b-122">La configuración de esta máquina virtual no es válida o no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="29a0b-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="29a0b-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="29a0b-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="29a0b-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="29a0b-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="29a0b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29a0b-125">Requirements</span></span>



| <span data-ttu-id="29a0b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="29a0b-126">Requirement</span></span> | <span data-ttu-id="29a0b-127">Value</span><span class="sxs-lookup"><span data-stu-id="29a0b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="29a0b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29a0b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="29a0b-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="29a0b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="29a0b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29a0b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="29a0b-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="29a0b-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="29a0b-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="29a0b-132">End of client support</span></span><br/>    | <span data-ttu-id="29a0b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="29a0b-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="29a0b-134">Producto</span><span class="sxs-lookup"><span data-stu-id="29a0b-134">Product</span></span><br/>                  | <span data-ttu-id="29a0b-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="29a0b-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="29a0b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29a0b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="29a0b-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="29a0b-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="29a0b-138">IID</span><span class="sxs-lookup"><span data-stu-id="29a0b-138">IID</span></span><br/>                      | <span data-ttu-id="29a0b-139">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="29a0b-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="29a0b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="29a0b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a0b-141">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="29a0b-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

