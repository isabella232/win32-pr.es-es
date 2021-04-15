---
title: Propiedad IVMGuestOS IsHeartbeating (VPCCOMInterfaces. h)
description: Determina si la máquina virtual tiene un latido.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Propiedad IsHeartbeating Virtual PC
- Propiedad IsHeartbeating Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad IsHeartbeating
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696043"
---
# <a name="ivmguestosisheartbeating-property"></a><span data-ttu-id="28c5e-106">IVMGuestOS:: IsHeartbeating (propiedad)</span><span class="sxs-lookup"><span data-stu-id="28c5e-106">IVMGuestOS::IsHeartbeating property</span></span>

<span data-ttu-id="28c5e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="28c5e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="28c5e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="28c5e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="28c5e-109">Determina si la máquina virtual tiene un latido.</span><span class="sxs-lookup"><span data-stu-id="28c5e-109">Determines whether the virtual machine has a heartbeat.</span></span>

<span data-ttu-id="28c5e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="28c5e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c5e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28c5e-111">Syntax</span></span>


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a><span data-ttu-id="28c5e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="28c5e-112">Property value</span></span>

<span data-ttu-id="28c5e-113">**Variante \_ TRUE** si se detecta un latido, **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="28c5e-113">**VARIANT\_TRUE** if a heartbeat is detected, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="28c5e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="28c5e-114">Error codes</span></span>



| <span data-ttu-id="28c5e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="28c5e-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="28c5e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="28c5e-116">Meaning</span></span>                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28c5e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="28c5e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="28c5e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="28c5e-118">The operation was successful.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="28c5e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="28c5e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="28c5e-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="28c5e-120">The parameter is **NULL**.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="28c5e-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="28c5e-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="28c5e-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="28c5e-122">The configuration is unknown.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="28c5e-123"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="28c5e-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="28c5e-124">La máquina virtual debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="28c5e-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="28c5e-125"><dt>Máquina virtual \_ E/s \_ \_ no \_ DISP</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="28c5e-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="28c5e-126">La máquina virtual no se ha iniciado completamente, la característica componentes de integración no está instalada o la versión instalada no es compatible con esta característica.</span><span class="sxs-lookup"><span data-stu-id="28c5e-126">The virtual machine is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="28c5e-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="28c5e-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="28c5e-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="28c5e-128">An unexpected error has occurred.</span></span><br/>                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="28c5e-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28c5e-129">Remarks</span></span>

<span data-ttu-id="28c5e-130">Cuando se instalan los componentes de integración en el sistema operativo invitado, se envía un "tick" o latido normal desde la sesión de máquina virtual a Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="28c5e-130">When integration components is installed in the guest operating system, a regular 'tick' or heartbeat is sent from the virtual machine session to Windows Virtual PC.</span></span> <span data-ttu-id="28c5e-131">Si el sistema operativo invitado está muy cargado, es posible que el equipo virtual reciba menos latidos de lo esperado.</span><span class="sxs-lookup"><span data-stu-id="28c5e-131">If the guest operating system is heavily loaded, it's possible that Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="28c5e-132">Si no se detecta ningún latido, es posible que el sistema operativo invitado no responda o se bloquee.</span><span class="sxs-lookup"><span data-stu-id="28c5e-132">If no heartbeat is detected, it is possible that the guest operating system is not responding or is crashed.</span></span>

<span data-ttu-id="28c5e-133">De forma predeterminada, una máquina virtual produce diez TICs de latido por minuto.</span><span class="sxs-lookup"><span data-stu-id="28c5e-133">By default, a virtual machine produces ten heartbeat ticks per minute.</span></span> <span data-ttu-id="28c5e-134">Si no se detectan TICs de latidos durante un minuto completo, Windows Virtual PC intentará reiniciar la sesión de máquina virtual una vez cada diez segundos durante un máximo de dos minutos.</span><span class="sxs-lookup"><span data-stu-id="28c5e-134">If no heartbeat ticks are detected for an entire minute, Windows Virtual PC will attempt to restart the virtual machine session once every ten seconds for up to two minutes.</span></span> <span data-ttu-id="28c5e-135">Este comportamiento se controla mediante los siguientes valores de clave en el archivo de configuración de la sesión de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="28c5e-135">This behavior is controlled by the following key values in the virtual machine session's configuration file.</span></span>



| <span data-ttu-id="28c5e-136">Clave de configuración</span><span class="sxs-lookup"><span data-stu-id="28c5e-136">Configuration key</span></span>                                            | <span data-ttu-id="28c5e-137">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="28c5e-137">Default</span></span>       | <span data-ttu-id="28c5e-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="28c5e-138">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c5e-139">integración/Microsoft/latido/hora</span><span class="sxs-lookup"><span data-stu-id="28c5e-139">integration/microsoft/heartbeat/time</span></span><br/>              | <span data-ttu-id="28c5e-140">60</span><span class="sxs-lookup"><span data-stu-id="28c5e-140">60</span></span><br/> | <span data-ttu-id="28c5e-141">La longitud del bloque de tiempo usado para generar TICs de latido, en segundos.</span><span class="sxs-lookup"><span data-stu-id="28c5e-141">The length of the block of time used to generate heartbeat ticks, in in seconds.</span></span><br/>                                             |
| <span data-ttu-id="28c5e-142">integración/Microsoft/latido/tasa</span><span class="sxs-lookup"><span data-stu-id="28c5e-142">integration/microsoft/heartbeat/rate</span></span><br/>              | <span data-ttu-id="28c5e-143">10</span><span class="sxs-lookup"><span data-stu-id="28c5e-143">10</span></span><br/> | <span data-ttu-id="28c5e-144">Número de pasos generados en cada bloque de tiempo de latido.</span><span class="sxs-lookup"><span data-stu-id="28c5e-144">The number of ticks generated in each heartbeat time block.</span></span><br/>                                                                  |
| <span data-ttu-id="28c5e-145">integración/Microsoft/latido/intervalo de errores \_</span><span class="sxs-lookup"><span data-stu-id="28c5e-145">integration/microsoft/heartbeat/failure\_interval</span></span><br/> | <span data-ttu-id="28c5e-146">10</span><span class="sxs-lookup"><span data-stu-id="28c5e-146">10</span></span><br/> | <span data-ttu-id="28c5e-147">El número de segundos entre los intentos de reinicio, una vez que no se reciben TICs de latido dentro de un bloque de tiempo de latido específico.</span><span class="sxs-lookup"><span data-stu-id="28c5e-147">The number of seconds between restart attempts, once no heartbeat ticks are received within a specific heartbeat time block.</span></span><br/> |
| <span data-ttu-id="28c5e-148">integración/Microsoft/latido/intentos de error \_</span><span class="sxs-lookup"><span data-stu-id="28c5e-148">integration/microsoft/heartbeat/failure\_attempts</span></span><br/> | <span data-ttu-id="28c5e-149">12</span><span class="sxs-lookup"><span data-stu-id="28c5e-149">12</span></span><br/> | <span data-ttu-id="28c5e-150">El número de intentos de reinicio realizados.</span><span class="sxs-lookup"><span data-stu-id="28c5e-150">The number of restart attempts made.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="28c5e-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c5e-151">Requirements</span></span>



| <span data-ttu-id="28c5e-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c5e-152">Requirement</span></span> | <span data-ttu-id="28c5e-153">Value</span><span class="sxs-lookup"><span data-stu-id="28c5e-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c5e-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28c5e-154">Minimum supported client</span></span><br/> | <span data-ttu-id="28c5e-155">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="28c5e-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28c5e-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28c5e-156">Minimum supported server</span></span><br/> | <span data-ttu-id="28c5e-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="28c5e-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="28c5e-158">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="28c5e-158">End of client support</span></span><br/>    | <span data-ttu-id="28c5e-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28c5e-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="28c5e-160">Producto</span><span class="sxs-lookup"><span data-stu-id="28c5e-160">Product</span></span><br/>                  | <span data-ttu-id="28c5e-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="28c5e-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="28c5e-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28c5e-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c5e-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c5e-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="28c5e-164">IID</span><span class="sxs-lookup"><span data-stu-id="28c5e-164">IID</span></span><br/>                      | <span data-ttu-id="28c5e-165">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="28c5e-165">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="28c5e-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="28c5e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c5e-167">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="28c5e-167">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

