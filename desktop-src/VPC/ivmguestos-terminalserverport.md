---
title: Propiedad TerminalServerPort de IVMGuestOS
description: Puerto usado por Servicios de Escritorio remoto en el sistema operativo invitado.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Propiedad TerminalServerPort Virtual PC
- Propiedad TerminalServerPort Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad TerminalServerPort
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150998"
---
# <a name="ivmguestosterminalserverport-property"></a><span data-ttu-id="04a77-106">IVMGuestOS:: TerminalServerPort (propiedad)</span><span class="sxs-lookup"><span data-stu-id="04a77-106">IVMGuestOS::TerminalServerPort property</span></span>

<span data-ttu-id="04a77-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="04a77-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="04a77-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="04a77-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="04a77-109">Puerto usado por Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="04a77-109">Port used by Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="04a77-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="04a77-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a77-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04a77-111">Syntax</span></span>


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a><span data-ttu-id="04a77-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="04a77-112">Property value</span></span>

<span data-ttu-id="04a77-113">Devuelve el puerto utilizado por Servicios de Escritorio remoto en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="04a77-113">Returns the port used by Remote Desktop Services in the guest operating system.</span></span>



| <span data-ttu-id="04a77-114">Value</span><span class="sxs-lookup"><span data-stu-id="04a77-114">Value</span></span>                                                                              | <span data-ttu-id="04a77-115">Significado</span><span class="sxs-lookup"><span data-stu-id="04a77-115">Meaning</span></span>                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="04a77-116"><dt>3389</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-116"><dt>3389</dt></span></span> </dl>    | <span data-ttu-id="04a77-117">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="04a77-117">Default value</span></span><br/>                      |
| <dl> <span data-ttu-id="04a77-118"><dt>1 65535</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-118"><dt>1 65535</dt></span></span> </dl> | <span data-ttu-id="04a77-119">Intervalo válido</span><span class="sxs-lookup"><span data-stu-id="04a77-119">Valid range</span></span><br/>                        |
| <dl> <span data-ttu-id="04a77-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-120"><dt>0</dt></span></span> </dl>       | <span data-ttu-id="04a77-121">El valor de Puerto válido no está disponible.</span><span class="sxs-lookup"><span data-stu-id="04a77-121">Valid port value is not available.</span></span><br/> |



 

## <a name="error-codes"></a><span data-ttu-id="04a77-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="04a77-122">Error codes</span></span>



| <span data-ttu-id="04a77-123">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="04a77-123">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="04a77-124">Significado</span><span class="sxs-lookup"><span data-stu-id="04a77-124">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04a77-125"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-125"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="04a77-126">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="04a77-126">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="04a77-127"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-127"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="04a77-128">Servicios de Escritorio remoto aún no se ha inicializado en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="04a77-128">Remote Desktop Services is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="04a77-129"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-129"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="04a77-130">El parámetro *tsPort* es **null**.</span><span class="sxs-lookup"><span data-stu-id="04a77-130">The *tsPort* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="04a77-131"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-131"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="04a77-132">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="04a77-132">The virtual machine is not running.</span></span><br/>                                           |
| <dl> <span data-ttu-id="04a77-133"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-133"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="04a77-134">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04a77-134">Integration components are not installed in this virtual machine.</span></span><br/>             |
| <dl> <span data-ttu-id="04a77-135"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-135"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="04a77-136">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="04a77-136">An unexpected error has occurred.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="04a77-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04a77-137">Remarks</span></span>

<span data-ttu-id="04a77-138">El valor de esta propiedad no es válido a menos que la propiedad [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) sea una **variante \_ verdadera**.</span><span class="sxs-lookup"><span data-stu-id="04a77-138">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="04a77-139">Si la propiedad [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) es una **variante \_ falsa** debido a un error de conexión en el puerto, el valor devuelto por la propiedad **TerminalServerPort** contiene el valor de error.</span><span class="sxs-lookup"><span data-stu-id="04a77-139">If the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_FALSE** due to a connection error on the port, then the value returned by the **TerminalServerPort** property contains the error value.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a77-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04a77-140">Requirements</span></span>



| <span data-ttu-id="04a77-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="04a77-141">Requirement</span></span> | <span data-ttu-id="04a77-142">Value</span><span class="sxs-lookup"><span data-stu-id="04a77-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a77-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04a77-143">Minimum supported client</span></span><br/> | <span data-ttu-id="04a77-144">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="04a77-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="04a77-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04a77-145">Minimum supported server</span></span><br/> | <span data-ttu-id="04a77-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="04a77-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="04a77-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="04a77-147">End of client support</span></span><br/>    | <span data-ttu-id="04a77-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04a77-148">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="04a77-149">IDL</span><span class="sxs-lookup"><span data-stu-id="04a77-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04a77-150"><dt>IVMGuestOS. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04a77-150"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="04a77-151">IID</span><span class="sxs-lookup"><span data-stu-id="04a77-151">IID</span></span><br/>                      | <span data-ttu-id="04a77-152">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="04a77-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="04a77-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="04a77-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a77-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="04a77-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

