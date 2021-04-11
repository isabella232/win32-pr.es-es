---
title: Método de cierre de sesión IVMGuestOS (VPCCOMInterfaces. h)
description: Cierra la sesión de todos los usuarios del sistema operativo invitado.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Logoff (método, equipo virtual PC)
- Logoff Method Virtual PC, IVMGuestOS (interfaz)
- Interfaz IVMGuestOS Virtual PC, método Logoff
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079731"
---
# <a name="ivmguestoslogoff-method"></a><span data-ttu-id="42dec-106">IVMGuestOS:: Logoff (método)</span><span class="sxs-lookup"><span data-stu-id="42dec-106">IVMGuestOS::Logoff method</span></span>

<span data-ttu-id="42dec-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="42dec-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="42dec-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="42dec-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="42dec-109">Cierra la sesión de todos los usuarios del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="42dec-109">Logs off all users from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="42dec-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42dec-110">Syntax</span></span>


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a><span data-ttu-id="42dec-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42dec-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42dec-112">*outLogoffTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="42dec-112">*outLogoffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="42dec-113">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de finalización de la secuencia de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="42dec-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the logoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42dec-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42dec-114">Return value</span></span>

<span data-ttu-id="42dec-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="42dec-115">This method can return one of these values.</span></span>



| <span data-ttu-id="42dec-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42dec-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="42dec-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="42dec-117">Description</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42dec-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42dec-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="42dec-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="42dec-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="42dec-120"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="42dec-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="42dec-121">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="42dec-121">An unexpected error has occurred.</span></span><br/>                                            |
| <dl> <span data-ttu-id="42dec-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="42dec-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="42dec-123">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="42dec-123">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="42dec-124"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="42dec-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="42dec-125">El autor de la llamada debe tener permisos de acceso de ejecución para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42dec-125">The caller must have execute access permissions for this VM.</span></span><br/>                 |
| <dl> <span data-ttu-id="42dec-126"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="42dec-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="42dec-127">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="42dec-127">The operation did not complete in a timely manner.</span></span><br/>                           |
| <dl> <span data-ttu-id="42dec-128"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="42dec-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="42dec-129">La característica componentes de integración no está instalada en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42dec-129">The integration components feature is not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="42dec-130"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="42dec-130"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="42dec-131">La máquina virtual (VM) debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="42dec-131">The virtual machine (VM) must be running for this operation.</span></span><br/>                 |
| <dl> <span data-ttu-id="42dec-132"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="42dec-132"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="42dec-133">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="42dec-133">The configuration is unknown.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="42dec-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42dec-134">Remarks</span></span>

<span data-ttu-id="42dec-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) se devuelve a través de la propiedad [**error**](ivmtask-error.md) del objeto [**IVMTask**](ivmtask.md) devuelto. no hay sesiones de inicio de sesión en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="42dec-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) is returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object there are no logon sessions in the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="42dec-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42dec-136">Requirements</span></span>



| <span data-ttu-id="42dec-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="42dec-137">Requirement</span></span> | <span data-ttu-id="42dec-138">Value</span><span class="sxs-lookup"><span data-stu-id="42dec-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42dec-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42dec-139">Minimum supported client</span></span><br/> | <span data-ttu-id="42dec-140">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="42dec-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42dec-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42dec-141">Minimum supported server</span></span><br/> | <span data-ttu-id="42dec-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="42dec-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="42dec-143">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="42dec-143">End of client support</span></span><br/>    | <span data-ttu-id="42dec-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42dec-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="42dec-145">Producto</span><span class="sxs-lookup"><span data-stu-id="42dec-145">Product</span></span><br/>                  | <span data-ttu-id="42dec-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="42dec-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="42dec-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42dec-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="42dec-148"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="42dec-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="42dec-149">IID</span><span class="sxs-lookup"><span data-stu-id="42dec-149">IID</span></span><br/>                      | <span data-ttu-id="42dec-150">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="42dec-150">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="42dec-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="42dec-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42dec-152">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="42dec-152">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

