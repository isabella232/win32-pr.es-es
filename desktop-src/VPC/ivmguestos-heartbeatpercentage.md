---
title: Propiedad IVMGuestOS HeartbeatPercentage (VPCCOMInterfaces. h)
description: Porcentaje de latidos esperados recibidos en el último minuto.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Propiedad HeartbeatPercentage Virtual PC
- Propiedad HeartbeatPercentage Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad HeartbeatPercentage
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535187"
---
# <a name="ivmguestosheartbeatpercentage-property"></a><span data-ttu-id="d9526-106">IVMGuestOS:: HeartbeatPercentage (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d9526-106">IVMGuestOS::HeartbeatPercentage property</span></span>

<span data-ttu-id="d9526-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d9526-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d9526-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d9526-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d9526-109">Recupera el porcentaje de latidos esperados recibidos en el último minuto.</span><span class="sxs-lookup"><span data-stu-id="d9526-109">Retrieves the percentage of expected heartbeats received over the past minute.</span></span>

<span data-ttu-id="d9526-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9526-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9526-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9526-111">Syntax</span></span>


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a><span data-ttu-id="d9526-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d9526-112">Property value</span></span>

<span data-ttu-id="d9526-113">Porcentaje de latidos esperados recibidos en el último minuto.</span><span class="sxs-lookup"><span data-stu-id="d9526-113">The percentage of expected heartbeats received over the past minute.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9526-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d9526-114">Error codes</span></span>



| <span data-ttu-id="d9526-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="d9526-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="d9526-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d9526-116">Meaning</span></span>                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9526-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d9526-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="d9526-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d9526-118">The operation was successful.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="d9526-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d9526-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="d9526-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="d9526-120">The parameter is **NULL**.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="d9526-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d9526-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="d9526-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="d9526-122">The configuration is unknown.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="d9526-123"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d9526-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="d9526-124">La máquina virtual (VM) debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="d9526-124">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="d9526-125"><dt>Máquina virtual \_ E/s \_ \_ no \_ DISP</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="d9526-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="d9526-126">La máquina virtual no se ha iniciado completamente, la característica componentes de integración no está instalada o la versión instalada no admite esta característica.</span><span class="sxs-lookup"><span data-stu-id="d9526-126">The VM is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="d9526-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d9526-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="d9526-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d9526-128">An unexpected error has occurred.</span></span><br/>                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="d9526-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9526-129">Remarks</span></span>

<span data-ttu-id="d9526-130">Los componentes de integración enviarán un latido periódico a Windows Virtual PC mientras se ejecuta el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="d9526-130">Integration components will send a periodic heartbeat to Windows Virtual PC while the guest operating system is running.</span></span> <span data-ttu-id="d9526-131">Si el sistema operativo invitado está muy cargado, es posible que Windows Virtual PC reciba menos latidos de lo esperado.</span><span class="sxs-lookup"><span data-stu-id="d9526-131">If the guest operating system is heavily loaded, it's possible that Windows Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="d9526-132">Si el porcentaje de latido desciende a cero, es posible que el sistema operativo invitado no responda o se bloquee.</span><span class="sxs-lookup"><span data-stu-id="d9526-132">If the heartbeat percentage drops to zero, it is possible that the guest operating system is not responding or is crashed.</span></span> <span data-ttu-id="d9526-133">La máquina virtual debe estar en ejecución (es decir, completamente arrancada y sin apagar) y los componentes de integración deben instalarse cuando se invoca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d9526-133">The virtual machine must be running (that is, fully booted and not shutting down) and integration components must be installed when this property is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9526-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9526-134">Requirements</span></span>



| <span data-ttu-id="d9526-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9526-135">Requirement</span></span> | <span data-ttu-id="d9526-136">Value</span><span class="sxs-lookup"><span data-stu-id="d9526-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9526-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9526-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d9526-138">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9526-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9526-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9526-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d9526-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d9526-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d9526-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d9526-141">End of client support</span></span><br/>    | <span data-ttu-id="d9526-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9526-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d9526-143">Producto</span><span class="sxs-lookup"><span data-stu-id="d9526-143">Product</span></span><br/>                  | <span data-ttu-id="d9526-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d9526-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d9526-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9526-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9526-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9526-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d9526-147">IID</span><span class="sxs-lookup"><span data-stu-id="d9526-147">IID</span></span><br/>                      | <span data-ttu-id="d9526-148">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="d9526-148">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d9526-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9526-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9526-150">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="d9526-150">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

