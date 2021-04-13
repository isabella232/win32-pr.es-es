---
title: Propiedad IVMGuestOS ComputerName (VPCCOMInterfaces. h)
description: El nombre de equipo del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: b35fa1a1-e105-43e6-9a2f-a5c7e71772cf
keywords:
- Propiedad ComputerName equipo virtual PC
- Propiedad ComputerName Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad ComputerName
topic_type:
- apiref
api_name:
- IVMGuestOS.ComputerName
- IVMGuestOS.get_ComputerName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b266c238809284b340095dd25390d6e5f3d2b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492898"
---
# <a name="ivmguestoscomputername-property"></a><span data-ttu-id="ed34e-106">Propiedad IVMGuestOS:: ComputerName</span><span class="sxs-lookup"><span data-stu-id="ed34e-106">IVMGuestOS::ComputerName property</span></span>

<span data-ttu-id="ed34e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ed34e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ed34e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ed34e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ed34e-109">Recupera el nombre de equipo del sistema operativo invitado que se ejecuta en la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="ed34e-109">Retrieves the computer name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="ed34e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed34e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed34e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed34e-111">Syntax</span></span>


```C++
HRESULT get_ComputerName(
  [out, retval] BSTR *guestComputerName
);
```



## <a name="property-value"></a><span data-ttu-id="ed34e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ed34e-112">Property value</span></span>

<span data-ttu-id="ed34e-113">El nombre de equipo del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="ed34e-113">The computer name of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ed34e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ed34e-114">Error codes</span></span>



| <span data-ttu-id="ed34e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="ed34e-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="ed34e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ed34e-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ed34e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ed34e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="ed34e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ed34e-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="ed34e-119"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ed34e-119"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="ed34e-120">El parámetro no es válido o no se ha especificado.</span><span class="sxs-lookup"><span data-stu-id="ed34e-120">The parameter is not valid or not specified.</span></span><br/>         |
| <dl> <span data-ttu-id="ed34e-121"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="ed34e-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="ed34e-122">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="ed34e-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="ed34e-123"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="ed34e-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="ed34e-124">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ed34e-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="ed34e-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ed34e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="ed34e-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ed34e-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="ed34e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed34e-127">Requirements</span></span>



| <span data-ttu-id="ed34e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed34e-128">Requirement</span></span> | <span data-ttu-id="ed34e-129">Value</span><span class="sxs-lookup"><span data-stu-id="ed34e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed34e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed34e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed34e-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed34e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed34e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed34e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed34e-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ed34e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ed34e-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ed34e-134">End of client support</span></span><br/>    | <span data-ttu-id="ed34e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed34e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ed34e-136">Producto</span><span class="sxs-lookup"><span data-stu-id="ed34e-136">Product</span></span><br/>                  | <span data-ttu-id="ed34e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ed34e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ed34e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed34e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed34e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed34e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ed34e-140">IID</span><span class="sxs-lookup"><span data-stu-id="ed34e-140">IID</span></span><br/>                      | <span data-ttu-id="ed34e-141">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="ed34e-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ed34e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed34e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed34e-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="ed34e-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

