---
title: Método IVMDVDDrive ReleaseImage (VPCCOMInterfaces. h)
description: Libera una imagen ISO capturada de la unidad de DVD.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- Método ReleaseImage Virtual PC
- Método ReleaseImage Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, método ReleaseImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a36a13b258d155760269399d9f25f5eda6f296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489340"
---
# <a name="ivmdvddrivereleaseimage-method"></a><span data-ttu-id="b6e4e-106">IVMDVDDrive:: ReleaseImage (método)</span><span class="sxs-lookup"><span data-stu-id="b6e4e-106">IVMDVDDrive::ReleaseImage method</span></span>

<span data-ttu-id="b6e4e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b6e4e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b6e4e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b6e4e-109">Libera una imagen ISO capturada de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-109">Releases a captured ISO image from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e4e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6e4e-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="b6e4e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6e4e-111">Parameters</span></span>

<span data-ttu-id="b6e4e-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6e4e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6e4e-113">Return value</span></span>

<span data-ttu-id="b6e4e-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b6e4e-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6e4e-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="b6e4e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6e4e-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6e4e-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b6e4e-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="b6e4e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b6e4e-119"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b6e4e-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="b6e4e-120">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-120">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="b6e4e-121"><dt>**Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="b6e4e-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="b6e4e-122">El medio capturado actualmente no es una unidad de disco del host.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-122">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="b6e4e-123"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b6e4e-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="b6e4e-124">No se pudo inicializar la unidad debido a una ubicación de bus no válida.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-124">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="b6e4e-125"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b6e4e-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="b6e4e-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b6e4e-126">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="b6e4e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6e4e-127">Requirements</span></span>



| <span data-ttu-id="b6e4e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e4e-128">Requirement</span></span> | <span data-ttu-id="b6e4e-129">Value</span><span class="sxs-lookup"><span data-stu-id="b6e4e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e4e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6e4e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e4e-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6e4e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6e4e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6e4e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e4e-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b6e4e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b6e4e-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b6e4e-134">End of client support</span></span><br/>    | <span data-ttu-id="b6e4e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6e4e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b6e4e-136">Producto</span><span class="sxs-lookup"><span data-stu-id="b6e4e-136">Product</span></span><br/>                  | <span data-ttu-id="b6e4e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b6e4e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b6e4e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6e4e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e4e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6e4e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b6e4e-140">IID</span><span class="sxs-lookup"><span data-stu-id="b6e4e-140">IID</span></span><br/>                      | <span data-ttu-id="b6e4e-141">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="b6e4e-141">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b6e4e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6e4e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e4e-143">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="b6e4e-143">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

