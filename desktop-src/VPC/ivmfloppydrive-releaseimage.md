---
title: Método IVMFloppyDrive ReleaseImage (VPCCOMInterfaces. h)
description: Libera una imagen de disquete en el host de la unidad de disquete.
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- Método ReleaseImage Virtual PC
- Método ReleaseImage Virtual PC, interfaz IVMFloppyDrive
- Interfaz IVMFloppyDrive Virtual PC, método ReleaseImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece899bbb615fc2d54a3cbdc86193e743168ef23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800974"
---
# <a name="ivmfloppydrivereleaseimage-method"></a><span data-ttu-id="3d8a3-106">IVMFloppyDrive:: ReleaseImage (método)</span><span class="sxs-lookup"><span data-stu-id="3d8a3-106">IVMFloppyDrive::ReleaseImage method</span></span>

<span data-ttu-id="3d8a3-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3d8a3-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3d8a3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3d8a3-109">Libera una imagen de disquete en el host de la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-109">Releases a floppy media image on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8a3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d8a3-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="3d8a3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d8a3-111">Parameters</span></span>

<span data-ttu-id="3d8a3-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d8a3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d8a3-113">Return value</span></span>

<span data-ttu-id="3d8a3-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3d8a3-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d8a3-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="3d8a3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d8a3-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d8a3-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a3-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="3d8a3-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="3d8a3-119"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3d8a3-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="3d8a3-120">La configuración de esta máquina virtual no es válida o no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="3d8a3-121"><dt>**Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a3-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="3d8a3-122">El medio conectado a esta unidad de disquete no es una imagen de disquete.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-122">The media attached to this floppy drive is not a floppy disk image.</span></span><br/>         |
| <dl> <span data-ttu-id="3d8a3-123"><dt>**Máquina virtual \_ E \_ no se ha \_ \_ capturado ningún medio**</dt> <dt>0xA00400652</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a3-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="3d8a3-124">No hay ningún medio conectado a esta unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="3d8a3-125"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a3-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="3d8a3-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3d8a3-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="3d8a3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d8a3-127">Requirements</span></span>



| <span data-ttu-id="3d8a3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d8a3-128">Requirement</span></span> | <span data-ttu-id="3d8a3-129">Value</span><span class="sxs-lookup"><span data-stu-id="3d8a3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8a3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d8a3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3d8a3-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d8a3-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d8a3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d8a3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3d8a3-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3d8a3-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3d8a3-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3d8a3-134">End of client support</span></span><br/>    | <span data-ttu-id="3d8a3-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d8a3-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3d8a3-136">Producto</span><span class="sxs-lookup"><span data-stu-id="3d8a3-136">Product</span></span><br/>                  | <span data-ttu-id="3d8a3-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3d8a3-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3d8a3-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d8a3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d8a3-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a3-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3d8a3-140">IID</span><span class="sxs-lookup"><span data-stu-id="3d8a3-140">IID</span></span><br/>                      | <span data-ttu-id="3d8a3-141">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="3d8a3-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3d8a3-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d8a3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8a3-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="3d8a3-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

