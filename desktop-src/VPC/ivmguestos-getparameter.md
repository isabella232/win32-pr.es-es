---
title: Método GetParameter de IVMGuestOS (VPCCOMInterfaces.h)
description: Recupera un parámetro con nombre dentro del sistema operativo invitado.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- Método GetParameter de Virtual PC
- Método GetParameter De PC virtual, interfaz IVMGuestOS
- IVMGuestOS interface Virtual PC , Método GetParameter
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
ms.openlocfilehash: d12bddec3fac5dc918f06d926fe5e5656b70d84d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387651"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="87551-106">IVMGuestOS::GetParameter (método)</span><span class="sxs-lookup"><span data-stu-id="87551-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="87551-107">\[Windows Virtual PC ya no está disponible para su uso a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="87551-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="87551-108">En su lugar, use el proveedor WMI de [Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="87551-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="87551-109">Recupera un parámetro con nombre dentro del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="87551-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="87551-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87551-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="87551-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87551-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87551-112">*inParameterName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="87551-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87551-113">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="87551-113">The parameter name.</span></span> <span data-ttu-id="87551-114">Debe tener entre 1 y 255 caracteres y no puede contener un carácter de barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="87551-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\\) character.</span></span>

</dd> <dt>

<span data-ttu-id="87551-115">*outParameterValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="87551-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="87551-116">Valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="87551-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87551-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87551-117">Return value</span></span>

<span data-ttu-id="87551-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="87551-118">This method can return one of these values.</span></span>



| <span data-ttu-id="87551-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87551-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="87551-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="87551-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87551-121"><dt>**S \_ Ok**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="87551-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="87551-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="87551-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="87551-123"><dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="87551-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="87551-124">Un parámetro no es válido o no se ha especificado.</span><span class="sxs-lookup"><span data-stu-id="87551-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="87551-125"><dt>**E \_ Puntero**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="87551-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="87551-126">El parámetro es **NULL.**</span><span class="sxs-lookup"><span data-stu-id="87551-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="87551-127"><dt>**Máquina virtual \_ Se \_ ha \_ 0xA0040202**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87551-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="87551-128">La operación no se ha completado a tiempo.</span><span class="sxs-lookup"><span data-stu-id="87551-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="87551-129"><dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="87551-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="87551-130">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="87551-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="87551-131"><dt>**Máquina virtual \_ E \_ VM \_ PAUSED**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="87551-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="87551-132">La máquina virtual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="87551-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="87551-133"><dt>**Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="87551-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="87551-134">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87551-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="87551-135"><dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="87551-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="87551-136">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="87551-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="87551-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87551-137">Remarks</span></span>

<span data-ttu-id="87551-138">La máquina virtual debe estar en ejecución y los componentes de integración deben instalarse cuando se invoca este método.</span><span class="sxs-lookup"><span data-stu-id="87551-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="87551-139">Este método solo se admite para sistemas operativos invitados basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="87551-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="87551-140">Con los componentes de integración instalados, la siguiente clave se agrega automáticamente al registro del sistema operativo invitado:</span><span class="sxs-lookup"><span data-stu-id="87551-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="87551-141">**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="87551-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="87551-142">Cuando se inicia el sistema operativo invitado, los siguientes valores de cadena del Registro se rellenan en la **clave** Parameters:</span><span class="sxs-lookup"><span data-stu-id="87551-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="87551-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="87551-143">**HostName**</span></span>
-   <span data-ttu-id="87551-144">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="87551-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="87551-145">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="87551-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="87551-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="87551-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="87551-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87551-147">Requirements</span></span>



| <span data-ttu-id="87551-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="87551-148">Requirement</span></span> | <span data-ttu-id="87551-149">Valor</span><span class="sxs-lookup"><span data-stu-id="87551-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="87551-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87551-150">Minimum supported client</span></span><br/> | <span data-ttu-id="87551-151">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="87551-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87551-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87551-152">Minimum supported server</span></span><br/> | <span data-ttu-id="87551-153">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="87551-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="87551-154">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="87551-154">End of client support</span></span><br/>    | <span data-ttu-id="87551-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="87551-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="87551-156">Producto</span><span class="sxs-lookup"><span data-stu-id="87551-156">Product</span></span><br/>                  | <span data-ttu-id="87551-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="87551-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="87551-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87551-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="87551-159"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="87551-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="87551-160">IID</span><span class="sxs-lookup"><span data-stu-id="87551-160">IID</span></span><br/>                      | <span data-ttu-id="87551-161">IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="87551-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="87551-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="87551-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87551-163">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="87551-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

