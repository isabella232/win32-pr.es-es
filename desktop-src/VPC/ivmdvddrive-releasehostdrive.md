---
title: Método IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libera una unidad de host capturada de la unidad de DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Método ReleaseHostDrive Virtual PC
- Método ReleaseHostDrive Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, método ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422203"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a><span data-ttu-id="ec901-106">IVMDVDDrive:: ReleaseHostDrive (método)</span><span class="sxs-lookup"><span data-stu-id="ec901-106">IVMDVDDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="ec901-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ec901-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ec901-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ec901-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ec901-109">Libera una unidad de host capturada de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="ec901-109">Releases a captured host drive from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec901-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec901-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="ec901-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec901-111">Parameters</span></span>

<span data-ttu-id="ec901-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ec901-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec901-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec901-113">Return value</span></span>

<span data-ttu-id="ec901-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ec901-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ec901-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec901-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="ec901-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec901-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec901-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ec901-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="ec901-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ec901-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ec901-119"><dt>**E \_ ERROR**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="ec901-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="ec901-120">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ec901-120">An unexpected error has occurred.</span></span><br/>                                  |
| <dl> <span data-ttu-id="ec901-121"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ec901-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="ec901-122">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ec901-122">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="ec901-123"><dt>**Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="ec901-123"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="ec901-124">El medio capturado actualmente no es una unidad de disco del host.</span><span class="sxs-lookup"><span data-stu-id="ec901-124">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="ec901-125"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ec901-125"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="ec901-126">No se pudo inicializar la unidad debido a una ubicación de bus no válida.</span><span class="sxs-lookup"><span data-stu-id="ec901-126">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="ec901-127"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ec901-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="ec901-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ec901-128">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="ec901-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec901-129">Requirements</span></span>



| <span data-ttu-id="ec901-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec901-130">Requirement</span></span> | <span data-ttu-id="ec901-131">Value</span><span class="sxs-lookup"><span data-stu-id="ec901-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec901-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec901-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ec901-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec901-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec901-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec901-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ec901-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ec901-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ec901-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ec901-136">End of client support</span></span><br/>    | <span data-ttu-id="ec901-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ec901-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ec901-138">Producto</span><span class="sxs-lookup"><span data-stu-id="ec901-138">Product</span></span><br/>                  | <span data-ttu-id="ec901-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ec901-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ec901-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec901-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec901-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec901-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ec901-142">IID</span><span class="sxs-lookup"><span data-stu-id="ec901-142">IID</span></span><br/>                      | <span data-ttu-id="ec901-143">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="ec901-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ec901-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec901-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec901-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="ec901-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

