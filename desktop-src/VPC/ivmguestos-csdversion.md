---
title: Propiedad IVMGuestOS CSDVersion (VPCCOMInterfaces. h)
description: El CSDVersion del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 6f1d8dd6-6feb-4bdf-a553-631d55c18076
keywords:
- Propiedad CSDVersion Virtual PC
- Propiedad CSDVersion Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad CSDVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.CSDVersion
- IVMGuestOS.get_CSDVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d82b3939f581edf328902f7fd0a26e1916abe1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997048"
---
# <a name="ivmguestoscsdversion-property"></a><span data-ttu-id="62112-106">IVMGuestOS:: CSDVersion (propiedad)</span><span class="sxs-lookup"><span data-stu-id="62112-106">IVMGuestOS::CSDVersion property</span></span>

<span data-ttu-id="62112-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="62112-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="62112-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="62112-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="62112-109">Recupera el CSDVersion del sistema operativo invitado que se ejecuta en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="62112-109">Retrieves the CSDVersion of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="62112-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="62112-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="62112-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62112-111">Syntax</span></span>


```C++
HRESULT get_CSDVersion(
  [out, retval] BSTR *csdVersion
);
```



## <a name="property-value"></a><span data-ttu-id="62112-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="62112-112">Property value</span></span>

<span data-ttu-id="62112-113">Una cadena terminada en null, como "Service Pack 3", que indica el último Service Pack instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="62112-113">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="62112-114">Si no se ha instalado ningún Service Pack, la cadena está vacía.</span><span class="sxs-lookup"><span data-stu-id="62112-114">If no Service Pack has been installed, the string is empty.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62112-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="62112-115">Error codes</span></span>



| <span data-ttu-id="62112-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="62112-116">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="62112-117">Significado</span><span class="sxs-lookup"><span data-stu-id="62112-117">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="62112-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="62112-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="62112-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="62112-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="62112-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="62112-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="62112-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="62112-121">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="62112-122"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="62112-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="62112-123">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="62112-123">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="62112-124"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="62112-124"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="62112-125">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="62112-125">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="62112-126"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="62112-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="62112-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="62112-127">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="62112-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62112-128">Requirements</span></span>



| <span data-ttu-id="62112-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="62112-129">Requirement</span></span> | <span data-ttu-id="62112-130">Value</span><span class="sxs-lookup"><span data-stu-id="62112-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62112-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62112-131">Minimum supported client</span></span><br/> | <span data-ttu-id="62112-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="62112-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62112-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62112-133">Minimum supported server</span></span><br/> | <span data-ttu-id="62112-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="62112-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="62112-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="62112-135">End of client support</span></span><br/>    | <span data-ttu-id="62112-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="62112-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="62112-137">Producto</span><span class="sxs-lookup"><span data-stu-id="62112-137">Product</span></span><br/>                  | <span data-ttu-id="62112-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="62112-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="62112-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62112-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="62112-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="62112-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="62112-141">IID</span><span class="sxs-lookup"><span data-stu-id="62112-141">IID</span></span><br/>                      | <span data-ttu-id="62112-142">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="62112-142">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="62112-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="62112-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62112-144">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="62112-144">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

