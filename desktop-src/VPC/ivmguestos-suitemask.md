---
title: Propiedad IVMGuestOS SuiteMask (VPCCOMInterfaces. h)
description: Recupera el SuiteMask del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Propiedad SuiteMask Virtual PC
- Propiedad SuiteMask Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad SuiteMask
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803842"
---
# <a name="ivmguestossuitemask-property"></a><span data-ttu-id="66660-106">IVMGuestOS:: SuiteMask (propiedad)</span><span class="sxs-lookup"><span data-stu-id="66660-106">IVMGuestOS::SuiteMask property</span></span>

<span data-ttu-id="66660-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="66660-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66660-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66660-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66660-109">Recupera el SuiteMask del sistema operativo invitado que se ejecuta en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66660-109">Retrieves the SuiteMask of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="66660-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="66660-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66660-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66660-111">Syntax</span></span>


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a><span data-ttu-id="66660-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="66660-112">Property value</span></span>

<span data-ttu-id="66660-113">Máscara del conjunto.</span><span class="sxs-lookup"><span data-stu-id="66660-113">The suite mask.</span></span> <span data-ttu-id="66660-114">Se admiten los siguientes valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="66660-114">The following string values are supported.</span></span>



| <span data-ttu-id="66660-115">Value</span><span class="sxs-lookup"><span data-stu-id="66660-115">Value</span></span>                                                                                   | <span data-ttu-id="66660-116">Significado</span><span class="sxs-lookup"><span data-stu-id="66660-116">Meaning</span></span>                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66660-117"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="66660-117"><dt>"0x00000004"</dt></span></span> </dl> | <span data-ttu-id="66660-118">Los componentes de Microsoft BackOffice están instalados.</span><span class="sxs-lookup"><span data-stu-id="66660-118">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="66660-119"><dt>"0x00000400"</dt></span><span class="sxs-lookup"><span data-stu-id="66660-119"><dt>"0x00000400"</dt></span></span> </dl> | <span data-ttu-id="66660-120">Windows Server 2003, Web Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="66660-120">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="66660-121"><dt>"0x00004000"</dt></span><span class="sxs-lookup"><span data-stu-id="66660-121"><dt>"0x00004000"</dt></span></span> </dl> | <span data-ttu-id="66660-122">Windows Server 2003, Compute Cluster Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="66660-122">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="66660-123"><dt>"0x00000080"</dt></span><span class="sxs-lookup"><span data-stu-id="66660-123"><dt>"0x00000080"</dt></span></span> </dl> | <span data-ttu-id="66660-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server están instalados.</span><span class="sxs-lookup"><span data-stu-id="66660-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/> |
| <dl> <span data-ttu-id="66660-125"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="66660-125"><dt>"0x00000002"</dt></span></span> </dl> | <span data-ttu-id="66660-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server están instalados.</span><span class="sxs-lookup"><span data-stu-id="66660-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span><br/>   |
| <dl> <span data-ttu-id="66660-127"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="66660-127"><dt>"0x00000040"</dt></span></span> </dl> | <span data-ttu-id="66660-128">Windows XP Embedded está instalado.</span><span class="sxs-lookup"><span data-stu-id="66660-128">Windows XP Embedded is installed.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="66660-129"><dt>"0x00000200"</dt></span><span class="sxs-lookup"><span data-stu-id="66660-129"><dt>"0x00000200"</dt></span></span> </dl> | <span data-ttu-id="66660-130">Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="66660-130">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="66660-131"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="66660-131"><dt>"0x00000100"</dt></span></span> </dl> | <span data-ttu-id="66660-132">Escritorio remoto es compatible, pero solo se admite una sesión interactiva.</span><span class="sxs-lookup"><span data-stu-id="66660-132">Remote Desktop is supported, but only one interactive session is supported.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="66660-133"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="66660-133"><dt>"0x00000001"</dt></span></span> </dl> | <span data-ttu-id="66660-134">Microsoft Small Business Server se ha instalado en el sistema, pero es posible que se haya actualizado a otra versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="66660-134">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span><br/>                                 |
| <dl> <span data-ttu-id="66660-135"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="66660-135"><dt>"0x00000020"</dt></span></span> </dl> | <span data-ttu-id="66660-136">Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor.</span><span class="sxs-lookup"><span data-stu-id="66660-136">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="66660-137"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="66660-137"><dt>"0x00002000"</dt></span></span> </dl> | <span data-ttu-id="66660-138">Windows Storage Server 2003 R2 o Windows Storage Server 2003 está instalado.</span><span class="sxs-lookup"><span data-stu-id="66660-138">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="66660-139"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="66660-139"><dt>"0x00000010"</dt></span></span> </dl> | <span data-ttu-id="66660-140">Servicios de Escritorio remoto está instalado.</span><span class="sxs-lookup"><span data-stu-id="66660-140">Remote Desktop Services is installed.</span></span> <span data-ttu-id="66660-141">Siempre se establece este valor.</span><span class="sxs-lookup"><span data-stu-id="66660-141">This value is always set.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="66660-142"><dt>"0x00008000"</dt></span><span class="sxs-lookup"><span data-stu-id="66660-142"><dt>"0x00008000"</dt></span></span> </dl> | <span data-ttu-id="66660-143">Windows Home Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="66660-143">Windows Home Server is installed.</span></span><br/>                                                                                                                           |



 

## <a name="error-codes"></a><span data-ttu-id="66660-144">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="66660-144">Error codes</span></span>



| <span data-ttu-id="66660-145">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="66660-145">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="66660-146">Significado</span><span class="sxs-lookup"><span data-stu-id="66660-146">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="66660-147"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66660-147"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="66660-148">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="66660-148">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="66660-149"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="66660-149"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="66660-150">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="66660-150">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="66660-151"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="66660-151"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="66660-152">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="66660-152">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="66660-153"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="66660-153"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="66660-154">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66660-154">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="66660-155"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="66660-155"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="66660-156">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="66660-156">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="66660-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66660-157">Requirements</span></span>



| <span data-ttu-id="66660-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="66660-158">Requirement</span></span> | <span data-ttu-id="66660-159">Value</span><span class="sxs-lookup"><span data-stu-id="66660-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66660-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66660-160">Minimum supported client</span></span><br/> | <span data-ttu-id="66660-161">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="66660-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66660-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66660-162">Minimum supported server</span></span><br/> | <span data-ttu-id="66660-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="66660-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66660-164">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="66660-164">End of client support</span></span><br/>    | <span data-ttu-id="66660-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66660-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66660-166">Producto</span><span class="sxs-lookup"><span data-stu-id="66660-166">Product</span></span><br/>                  | <span data-ttu-id="66660-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66660-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66660-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66660-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="66660-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="66660-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66660-170">IID</span><span class="sxs-lookup"><span data-stu-id="66660-170">IID</span></span><br/>                      | <span data-ttu-id="66660-171">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="66660-171">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="66660-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="66660-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66660-173">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="66660-173">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

