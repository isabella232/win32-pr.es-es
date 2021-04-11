---
title: Propiedad MultipleUserSessionsAllowed de IVMGuestOS
description: Determina si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Propiedad MultipleUserSessionsAllowed Virtual PC
- Propiedad MultipleUserSessionsAllowed Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad MultipleUserSessionsAllowed
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150382"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a><span data-ttu-id="a6980-106">IVMGuestOS:: MultipleUserSessionsAllowed (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a6980-106">IVMGuestOS::MultipleUserSessionsAllowed property</span></span>

<span data-ttu-id="a6980-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a6980-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a6980-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a6980-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a6980-109">Determina si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="a6980-109">Determines whether multiple simultaneous user sessions are allowed in the guest operating system.</span></span>

<span data-ttu-id="a6980-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6980-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6980-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6980-111">Syntax</span></span>


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a><span data-ttu-id="a6980-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a6980-112">Property value</span></span>

<span data-ttu-id="a6980-113">**Variante \_ TRUE** si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado, **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a6980-113">**VARIANT\_TRUE** if multiple simultaneous user sessions are allowed in the guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a6980-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a6980-114">Error codes</span></span>



| <span data-ttu-id="a6980-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="a6980-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="a6980-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a6980-116">Meaning</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6980-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a6980-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="a6980-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6980-118">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="a6980-119"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a6980-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="a6980-120">Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) aún no se ha inicializado en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="a6980-120">Remote Desktop Services (formerly known as Terminal Services) is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="a6980-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a6980-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="a6980-122">El parámetro *sessionStatus* es **null**.</span><span class="sxs-lookup"><span data-stu-id="a6980-122">The *sessionStatus* parameter is **NULL**.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="a6980-123"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="a6980-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="a6980-124">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a6980-124">The virtual machine is not running.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a6980-125"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="a6980-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="a6980-126">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a6980-126">Integration components are not installed in this virtual machine.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="a6980-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a6980-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="a6980-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a6980-128">An unexpected error has occurred.</span></span><br/>                                                                                   |



## <a name="remarks"></a><span data-ttu-id="a6980-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6980-129">Remarks</span></span>

<span data-ttu-id="a6980-130">El valor de esta propiedad no es válido a menos que la propiedad [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) sea una **variante \_ verdadera**.</span><span class="sxs-lookup"><span data-stu-id="a6980-130">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="a6980-131">En el caso de los sistemas operativos de cliente de Windows, **MultipleUserSessionsAllowed** es **Variant \_ true** si se admite el cambio rápido de usuario.</span><span class="sxs-lookup"><span data-stu-id="a6980-131">For Windows client operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Fast User Switching is supported.</span></span> <span data-ttu-id="a6980-132">En el caso de los sistemas operativos Windows Server, **MultipleUserSessionsAllowed** es **VARIANT \_ true** si servicios de escritorio remoto (anteriormente denominado Terminal Services) está instalado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="a6980-132">For Windows Server operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Remote Desktop Services (formerly called Terminal Services) is installed and enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6980-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6980-133">Requirements</span></span>



| <span data-ttu-id="a6980-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6980-134">Requirement</span></span> | <span data-ttu-id="a6980-135">Value</span><span class="sxs-lookup"><span data-stu-id="a6980-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6980-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6980-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a6980-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6980-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a6980-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6980-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a6980-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a6980-139">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a6980-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a6980-140">End of client support</span></span><br/>    | <span data-ttu-id="a6980-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6980-141">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="a6980-142">IDL</span><span class="sxs-lookup"><span data-stu-id="a6980-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6980-143"><dt>IVMGuestOS. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6980-143"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6980-144">IID</span><span class="sxs-lookup"><span data-stu-id="a6980-144">IID</span></span><br/>                      | <span data-ttu-id="a6980-145">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="a6980-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a6980-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6980-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6980-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="a6980-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

