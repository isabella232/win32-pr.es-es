---
title: Método GetParameter IVMGuestOS (VPCCOMInterfaces. h)
description: Recupera un parámetro con nombre dentro del sistema operativo invitado.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- GetParameter (método, equipo virtual PC)
- Método GetParameter Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método GetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535182"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="933c1-106">IVMGuestOS:: GetParameter (método)</span><span class="sxs-lookup"><span data-stu-id="933c1-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="933c1-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="933c1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="933c1-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="933c1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="933c1-109">Recupera un parámetro con nombre dentro del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="933c1-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="933c1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="933c1-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="933c1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="933c1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933c1-112">*inParameterName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="933c1-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="933c1-113">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="933c1-113">The parameter name.</span></span> <span data-ttu-id="933c1-114">Debe tener entre 1 y 255 caracteres de longitud y no puede contener una barra diagonal inversa ( \) carácter.</span><span class="sxs-lookup"><span data-stu-id="933c1-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="933c1-115">*outParameterValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="933c1-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="933c1-116">Valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="933c1-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933c1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="933c1-117">Return value</span></span>

<span data-ttu-id="933c1-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="933c1-118">This method can return one of these values.</span></span>



| <span data-ttu-id="933c1-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="933c1-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="933c1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="933c1-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="933c1-121"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="933c1-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="933c1-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="933c1-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="933c1-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="933c1-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="933c1-124">Un parámetro no es válido o no se ha especificado.</span><span class="sxs-lookup"><span data-stu-id="933c1-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="933c1-125"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="933c1-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="933c1-126">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="933c1-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="933c1-127"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="933c1-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="933c1-128">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="933c1-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="933c1-129"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="933c1-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="933c1-130">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="933c1-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="933c1-131"><dt>**Máquina virtual \_ E/s de \_ VM en \_ pausa**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="933c1-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="933c1-132">La máquina virtual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="933c1-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="933c1-133"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="933c1-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="933c1-134">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="933c1-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="933c1-135"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="933c1-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="933c1-136">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="933c1-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="933c1-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="933c1-137">Remarks</span></span>

<span data-ttu-id="933c1-138">La máquina virtual debe estar en ejecución y los componentes de integración deben instalarse cuando se invoca este método.</span><span class="sxs-lookup"><span data-stu-id="933c1-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="933c1-139">Este método solo es compatible con sistemas operativos invitados basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="933c1-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="933c1-140">Con los componentes de integración de instalados, se agrega automáticamente la clave siguiente al registro del sistema operativo invitado:</span><span class="sxs-lookup"><span data-stu-id="933c1-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="933c1-141">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="933c1-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="933c1-142">Cuando se inicia el sistema operativo invitado, los siguientes valores de cadena del registro se rellenan en la clave **Parameters** :</span><span class="sxs-lookup"><span data-stu-id="933c1-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="933c1-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="933c1-143">**HostName**</span></span>
-   <span data-ttu-id="933c1-144">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="933c1-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="933c1-145">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="933c1-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="933c1-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="933c1-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="933c1-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="933c1-147">Requirements</span></span>



| <span data-ttu-id="933c1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="933c1-148">Requirement</span></span> | <span data-ttu-id="933c1-149">Value</span><span class="sxs-lookup"><span data-stu-id="933c1-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="933c1-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="933c1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="933c1-151">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="933c1-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="933c1-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="933c1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="933c1-153">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="933c1-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="933c1-154">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="933c1-154">End of client support</span></span><br/>    | <span data-ttu-id="933c1-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="933c1-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="933c1-156">Producto</span><span class="sxs-lookup"><span data-stu-id="933c1-156">Product</span></span><br/>                  | <span data-ttu-id="933c1-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="933c1-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="933c1-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="933c1-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="933c1-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="933c1-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="933c1-160">IID</span><span class="sxs-lookup"><span data-stu-id="933c1-160">IID</span></span><br/>                      | <span data-ttu-id="933c1-161">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="933c1-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="933c1-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="933c1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933c1-163">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="933c1-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

