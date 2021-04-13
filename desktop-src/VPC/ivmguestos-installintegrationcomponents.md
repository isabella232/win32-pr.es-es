---
title: Método IVMGuestOS InstallIntegrationComponents (VPCCOMInterfaces. h)
description: Busca e instala los componentes de integración más recientes en el sistema operativo invitado.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- Método InstallIntegrationComponents Virtual PC
- Método InstallIntegrationComponents Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método InstallIntegrationComponents
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421957"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a><span data-ttu-id="506d9-106">IVMGuestOS:: InstallIntegrationComponents (método)</span><span class="sxs-lookup"><span data-stu-id="506d9-106">IVMGuestOS::InstallIntegrationComponents method</span></span>

<span data-ttu-id="506d9-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="506d9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="506d9-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="506d9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="506d9-109">Busca e instala los componentes de integración más recientes en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="506d9-109">Locates and installs the latest Integration Components into the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="506d9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="506d9-110">Syntax</span></span>


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a><span data-ttu-id="506d9-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="506d9-111">Parameters</span></span>

<span data-ttu-id="506d9-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="506d9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="506d9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="506d9-113">Return value</span></span>

<span data-ttu-id="506d9-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="506d9-114">This method can return one of these values.</span></span>



| <span data-ttu-id="506d9-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="506d9-115">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="506d9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="506d9-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="506d9-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="506d9-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="506d9-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="506d9-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="506d9-119"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="506d9-119"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                       | <span data-ttu-id="506d9-120">La máquina virtual debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="506d9-120">The virtual machine must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="506d9-121"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="506d9-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="506d9-122">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="506d9-122">The virtual machine could not be found.</span></span><br/>                                     |
| <dl> <span data-ttu-id="506d9-123"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="506d9-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="506d9-124">La máquina virtual no tiene una unidad de DVD vacía.</span><span class="sxs-lookup"><span data-stu-id="506d9-124">The virtual machine does not have an empty DVD drive.</span></span><br/>                       |
| <dl> <span data-ttu-id="506d9-125"><dt>**Máquina virtual \_ \_Error de \_ desmontaje \_ de medios E**</dt> <dt>0xA0040508</dt></span><span class="sxs-lookup"><span data-stu-id="506d9-125"><dt>**VM\_E\_MEDIA\_UNMOUNT\_FAIL**</dt> <dt>0xA0040508</dt></span></span> </dl>                   | <span data-ttu-id="506d9-126">Error al intentar desmontar el medio de la unidad de DVD de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="506d9-126">The attempt to unmount the media from the virtual machine DVD drive failed.</span></span><br/> |
| <dl> <span data-ttu-id="506d9-127"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="506d9-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="506d9-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="506d9-128">An unexpected error has occurred.</span></span><br/>                                           |
| <dl> <span data-ttu-id="506d9-129"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="506d9-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="506d9-130">El sistema no puede encontrar el archivo ISO para los componentes de integración.</span><span class="sxs-lookup"><span data-stu-id="506d9-130">The system cannot find the ISO file for the Integration Components.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="506d9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="506d9-131">Requirements</span></span>



| <span data-ttu-id="506d9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="506d9-132">Requirement</span></span> | <span data-ttu-id="506d9-133">Value</span><span class="sxs-lookup"><span data-stu-id="506d9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="506d9-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="506d9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="506d9-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="506d9-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="506d9-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="506d9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="506d9-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="506d9-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="506d9-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="506d9-138">End of client support</span></span><br/>    | <span data-ttu-id="506d9-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="506d9-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="506d9-140">Producto</span><span class="sxs-lookup"><span data-stu-id="506d9-140">Product</span></span><br/>                  | <span data-ttu-id="506d9-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="506d9-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="506d9-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="506d9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="506d9-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="506d9-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="506d9-144">IID</span><span class="sxs-lookup"><span data-stu-id="506d9-144">IID</span></span><br/>                      | <span data-ttu-id="506d9-145">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="506d9-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="506d9-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="506d9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506d9-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="506d9-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

