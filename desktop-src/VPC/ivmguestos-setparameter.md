---
title: Método SetParameter de IVMGuestOS (VPCCOMInterfaces.h)
description: Establece un parámetro con nombre dentro del sistema operativo invitado.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- SetParameter method Virtual PC
- SetParameter method Virtual PC , IVMGuestOS interface
- IVMGuestOS interface Virtual PC , SetParameter method
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
ms.openlocfilehash: 2cc99d9b38ab43327b4a435c4128378d49682935
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386714"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="63643-106">IVMGuestOS::SetParameter (método)</span><span class="sxs-lookup"><span data-stu-id="63643-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="63643-107">\[Windows Virtual PC ya no está disponible para su uso a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63643-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63643-108">En su lugar, use el proveedor WMI de [Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="63643-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63643-109">Establece un parámetro con nombre dentro del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="63643-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="63643-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63643-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="63643-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63643-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63643-112">*inParameterName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="63643-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63643-113">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="63643-113">The parameter name.</span></span> <span data-ttu-id="63643-114">Debe tener entre 1 y 255 caracteres y no puede contener un carácter de barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="63643-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\\) character.</span></span>

</dd> <dt>

<span data-ttu-id="63643-115">*inParameterValue* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="63643-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63643-116">Valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="63643-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63643-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63643-117">Return value</span></span>

<span data-ttu-id="63643-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="63643-118">This method can return one of these values.</span></span>



| <span data-ttu-id="63643-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63643-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="63643-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="63643-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="63643-121"><dt>**S \_ Ok**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63643-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="63643-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="63643-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="63643-123"><dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="63643-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="63643-124">Un parámetro no es válido o no se ha especificado.</span><span class="sxs-lookup"><span data-stu-id="63643-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="63643-125"><dt>**Máquina virtual \_ Se \_ ha \_ 0xA0040202**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="63643-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="63643-126">La operación no se ha completado a tiempo.</span><span class="sxs-lookup"><span data-stu-id="63643-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="63643-127"><dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="63643-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="63643-128">La máquina virtual (VM) no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="63643-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="63643-129"><dt>**Máquina virtual \_ E \_ VM \_ PAUSED**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="63643-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="63643-130">La máquina virtual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="63643-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="63643-131"><dt>**Máquina virtual \_ LA \_ CARACTERÍSTICA DE \_ ADICIONES \_ NO \_ ESTÁ**</dt> DISPONIBLE <dt>0XA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="63643-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="63643-132">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="63643-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="63643-133"><dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="63643-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="63643-134">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="63643-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="63643-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63643-135">Remarks</span></span>

<span data-ttu-id="63643-136">La máquina virtual debe estar en ejecución y los componentes de integración deben instalarse cuando se invoca este método.</span><span class="sxs-lookup"><span data-stu-id="63643-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="63643-137">Este método solo se admite para sistemas operativos invitados basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="63643-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="63643-138">Con los componentes de integración instalados, la siguiente clave se agrega automáticamente al registro del sistema operativo invitado:</span><span class="sxs-lookup"><span data-stu-id="63643-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="63643-139">**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="63643-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="63643-140">Cuando se inicia el sistema operativo invitado, los siguientes valores de cadena del Registro se rellenan en la **clave** Parameters:</span><span class="sxs-lookup"><span data-stu-id="63643-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="63643-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="63643-141">**HostName**</span></span>
-   <span data-ttu-id="63643-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="63643-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="63643-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="63643-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="63643-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="63643-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="63643-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63643-145">Requirements</span></span>



| <span data-ttu-id="63643-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="63643-146">Requirement</span></span> | <span data-ttu-id="63643-147">Valor</span><span class="sxs-lookup"><span data-stu-id="63643-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63643-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63643-148">Minimum supported client</span></span><br/> | <span data-ttu-id="63643-149">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="63643-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63643-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63643-150">Minimum supported server</span></span><br/> | <span data-ttu-id="63643-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="63643-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="63643-152">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="63643-152">End of client support</span></span><br/>    | <span data-ttu-id="63643-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63643-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="63643-154">Producto</span><span class="sxs-lookup"><span data-stu-id="63643-154">Product</span></span><br/>                  | <span data-ttu-id="63643-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63643-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="63643-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63643-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="63643-157"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="63643-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="63643-158">IID</span><span class="sxs-lookup"><span data-stu-id="63643-158">IID</span></span><br/>                      | <span data-ttu-id="63643-159">IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="63643-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="63643-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="63643-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63643-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="63643-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

