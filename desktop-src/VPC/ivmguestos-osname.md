---
title: Propiedad IVMGuestOS OSName (VPCCOMInterfaces. h)
description: Nombre del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- Propiedad OSName Virtual PC
- Propiedad OSName Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad OSName
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672c7b2c852bcbb1ec39b61889b03738e3a2df23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490445"
---
# <a name="ivmguestososname-property"></a><span data-ttu-id="c1881-106">IVMGuestOS:: OSName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c1881-106">IVMGuestOS::OSName property</span></span>

<span data-ttu-id="c1881-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c1881-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c1881-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c1881-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c1881-109">Recupera el nombre del sistema operativo invitado que se ejecuta en la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="c1881-109">Retrieves the name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="c1881-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c1881-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1881-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1881-111">Syntax</span></span>


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a><span data-ttu-id="c1881-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c1881-112">Property value</span></span>

<span data-ttu-id="c1881-113">Nombre completo (incluido el nombre de conjunto) del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="c1881-113">The full name (including suite name) of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c1881-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c1881-114">Error codes</span></span>



| <span data-ttu-id="c1881-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="c1881-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="c1881-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c1881-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c1881-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c1881-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="c1881-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c1881-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="c1881-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c1881-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="c1881-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="c1881-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="c1881-121"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="c1881-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="c1881-122">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="c1881-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="c1881-123"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="c1881-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="c1881-124">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1881-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="c1881-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c1881-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="c1881-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="c1881-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="c1881-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1881-127">Remarks</span></span>

<span data-ttu-id="c1881-128">La máquina virtual debe estar en ejecución (es decir, completamente arrancada y sin apagar) y los componentes de integración deben instalarse cuando se invoca este método.</span><span class="sxs-lookup"><span data-stu-id="c1881-128">The VM must be running (that is, fully booted and not shutting down) and integration components must be installed when this method is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1881-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1881-129">Requirements</span></span>



| <span data-ttu-id="c1881-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1881-130">Requirement</span></span> | <span data-ttu-id="c1881-131">Value</span><span class="sxs-lookup"><span data-stu-id="c1881-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1881-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1881-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c1881-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1881-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1881-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1881-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c1881-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c1881-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c1881-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c1881-136">End of client support</span></span><br/>    | <span data-ttu-id="c1881-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1881-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c1881-138">Producto</span><span class="sxs-lookup"><span data-stu-id="c1881-138">Product</span></span><br/>                  | <span data-ttu-id="c1881-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c1881-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c1881-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1881-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1881-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1881-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c1881-142">IID</span><span class="sxs-lookup"><span data-stu-id="c1881-142">IID</span></span><br/>                      | <span data-ttu-id="c1881-143">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="c1881-143">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c1881-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1881-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1881-145">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="c1881-145">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

