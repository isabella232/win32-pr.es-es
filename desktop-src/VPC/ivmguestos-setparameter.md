---
title: Método IVMGuestOS SetParameter (VPCCOMInterfaces. h)
description: Establece un parámetro con nombre dentro del sistema operativo invitado.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Método SetParameter Virtual PC
- Método SetParameter Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método SetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534282"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="60a10-106">IVMGuestOS:: SetParameter (método)</span><span class="sxs-lookup"><span data-stu-id="60a10-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="60a10-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="60a10-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="60a10-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="60a10-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="60a10-109">Establece un parámetro con nombre dentro del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="60a10-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a10-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60a10-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="60a10-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60a10-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60a10-112">*inParameterName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60a10-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60a10-113">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="60a10-113">The parameter name.</span></span> <span data-ttu-id="60a10-114">Debe tener entre 1 y 255 caracteres de longitud y no puede contener una barra diagonal inversa ( \) carácter.</span><span class="sxs-lookup"><span data-stu-id="60a10-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="60a10-115">*inParameterValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60a10-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60a10-116">Valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="60a10-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60a10-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60a10-117">Return value</span></span>

<span data-ttu-id="60a10-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="60a10-118">This method can return one of these values.</span></span>



| <span data-ttu-id="60a10-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60a10-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="60a10-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="60a10-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="60a10-121"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="60a10-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="60a10-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="60a10-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="60a10-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="60a10-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="60a10-124">Un parámetro no es válido o no se ha especificado.</span><span class="sxs-lookup"><span data-stu-id="60a10-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="60a10-125"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="60a10-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="60a10-126">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="60a10-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="60a10-127"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="60a10-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="60a10-128">La máquina virtual (VM) no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="60a10-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="60a10-129"><dt>**Máquina virtual \_ E/s de \_ VM en \_ pausa**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="60a10-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="60a10-130">La máquina virtual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="60a10-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="60a10-131"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="60a10-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="60a10-132">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="60a10-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="60a10-133"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="60a10-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="60a10-134">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="60a10-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="60a10-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60a10-135">Remarks</span></span>

<span data-ttu-id="60a10-136">La máquina virtual debe estar en ejecución y los componentes de integración deben instalarse cuando se invoca este método.</span><span class="sxs-lookup"><span data-stu-id="60a10-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="60a10-137">Este método solo es compatible con sistemas operativos invitados basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="60a10-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="60a10-138">Con los componentes de integración de instalados, se agrega automáticamente la clave siguiente al registro del sistema operativo invitado:</span><span class="sxs-lookup"><span data-stu-id="60a10-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="60a10-139">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="60a10-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="60a10-140">Cuando se inicia el sistema operativo invitado, los siguientes valores de cadena del registro se rellenan en la clave **Parameters** :</span><span class="sxs-lookup"><span data-stu-id="60a10-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="60a10-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="60a10-141">**HostName**</span></span>
-   <span data-ttu-id="60a10-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="60a10-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="60a10-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="60a10-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="60a10-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="60a10-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="60a10-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60a10-145">Requirements</span></span>



| <span data-ttu-id="60a10-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="60a10-146">Requirement</span></span> | <span data-ttu-id="60a10-147">Value</span><span class="sxs-lookup"><span data-stu-id="60a10-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="60a10-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60a10-148">Minimum supported client</span></span><br/> | <span data-ttu-id="60a10-149">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="60a10-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60a10-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60a10-150">Minimum supported server</span></span><br/> | <span data-ttu-id="60a10-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="60a10-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="60a10-152">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="60a10-152">End of client support</span></span><br/>    | <span data-ttu-id="60a10-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="60a10-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="60a10-154">Producto</span><span class="sxs-lookup"><span data-stu-id="60a10-154">Product</span></span><br/>                  | <span data-ttu-id="60a10-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="60a10-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="60a10-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60a10-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="60a10-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="60a10-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="60a10-158">IID</span><span class="sxs-lookup"><span data-stu-id="60a10-158">IID</span></span><br/>                      | <span data-ttu-id="60a10-159">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="60a10-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="60a10-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="60a10-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a10-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="60a10-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

