---
title: Propiedad IVMGuestOS TerminalServicesInitialized (VPCCOMInterfaces. h)
description: Estado de Servicios de Escritorio remoto en el sistema operativo invitado.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- Propiedad TerminalServicesInitialized Virtual PC
- Propiedad TerminalServicesInitialized Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad TerminalServicesInitialized
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92ce23b4b07f3e2d06f605f4598c8b31e4c70692
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535302"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a><span data-ttu-id="ccf83-106">IVMGuestOS:: TerminalServicesInitialized (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ccf83-106">IVMGuestOS::TerminalServicesInitialized property</span></span>

<span data-ttu-id="ccf83-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ccf83-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ccf83-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ccf83-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ccf83-109">Recupera el estado de Servicios de Escritorio remoto (antes conocido como Terminal Services) en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="ccf83-109">Retrieves the status of Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="ccf83-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ccf83-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf83-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccf83-111">Syntax</span></span>


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a><span data-ttu-id="ccf83-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ccf83-112">Property value</span></span>

<span data-ttu-id="ccf83-113">Estado de inicialización.</span><span class="sxs-lookup"><span data-stu-id="ccf83-113">The initialization status.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccf83-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ccf83-114">Error codes</span></span>



| <span data-ttu-id="ccf83-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="ccf83-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="ccf83-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ccf83-116">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ccf83-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ccf83-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="ccf83-118">La operación se realizó correctamente y se ha inicializado Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ccf83-118">The operation was successful and Remote Desktop Services has been initialized.</span></span> <span data-ttu-id="ccf83-119">El valor de propiedad devuelto indica si Servicios de Escritorio remoto está disponible en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="ccf83-119">The returned property value indicates whether Remote Desktop Services is available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="ccf83-120"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ccf83-120"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="ccf83-121">La característica componentes de integración se está ejecutando, pero aún no se ha inicializado Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ccf83-121">The integration components feature is running, but Remote Desktop Services is not yet initialized.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="ccf83-122"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ccf83-122"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="ccf83-123">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="ccf83-123">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="ccf83-124"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="ccf83-124"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="ccf83-125">La máquina virtual (VM) debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="ccf83-125">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="ccf83-126"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="ccf83-126"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="ccf83-127">La característica componentes de integración no se está ejecutando en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="ccf83-127">The integration components feature is not running in the guest operating system.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="ccf83-128"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ccf83-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="ccf83-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ccf83-129">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="ccf83-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccf83-130">Requirements</span></span>



| <span data-ttu-id="ccf83-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf83-131">Requirement</span></span> | <span data-ttu-id="ccf83-132">Value</span><span class="sxs-lookup"><span data-stu-id="ccf83-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf83-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccf83-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf83-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccf83-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ccf83-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccf83-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf83-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ccf83-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ccf83-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ccf83-137">End of client support</span></span><br/>    | <span data-ttu-id="ccf83-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ccf83-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ccf83-139">Producto</span><span class="sxs-lookup"><span data-stu-id="ccf83-139">Product</span></span><br/>                  | <span data-ttu-id="ccf83-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ccf83-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ccf83-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccf83-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccf83-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf83-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ccf83-143">IID</span><span class="sxs-lookup"><span data-stu-id="ccf83-143">IID</span></span><br/>                      | <span data-ttu-id="ccf83-144">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="ccf83-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ccf83-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccf83-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf83-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="ccf83-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

