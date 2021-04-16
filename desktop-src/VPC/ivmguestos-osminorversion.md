---
title: Propiedad IVMGuestOS OSMinorVersion (VPCCOMInterfaces. h)
description: La versión secundaria del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: fa71e215-8633-4f53-ab71-bc9bfdb56cc8
keywords:
- Propiedad OSMinorVersion Virtual PC
- Propiedad OSMinorVersion Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad OSMinorVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMinorVersion
- IVMGuestOS.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c068ee6d8112561f57d0644f6bc7bc4844096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695932"
---
# <a name="ivmguestososminorversion-property"></a><span data-ttu-id="cb44e-106">IVMGuestOS:: OSMinorVersion (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cb44e-106">IVMGuestOS::OSMinorVersion property</span></span>

<span data-ttu-id="cb44e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cb44e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cb44e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cb44e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cb44e-109">Recupera la versión secundaria del sistema operativo invitado que se ejecuta en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb44e-109">Retrieves the minor version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="cb44e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cb44e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb44e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb44e-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] BSTR *minorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="cb44e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cb44e-112">Property value</span></span>

<span data-ttu-id="cb44e-113">Versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="cb44e-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb44e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="cb44e-114">Error codes</span></span>



| <span data-ttu-id="cb44e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="cb44e-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="cb44e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="cb44e-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cb44e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cb44e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="cb44e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cb44e-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="cb44e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cb44e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="cb44e-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="cb44e-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="cb44e-121"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="cb44e-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="cb44e-122">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="cb44e-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="cb44e-123"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="cb44e-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="cb44e-124">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb44e-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="cb44e-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cb44e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="cb44e-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="cb44e-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="cb44e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb44e-127">Requirements</span></span>



| <span data-ttu-id="cb44e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb44e-128">Requirement</span></span> | <span data-ttu-id="cb44e-129">Value</span><span class="sxs-lookup"><span data-stu-id="cb44e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb44e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb44e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cb44e-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb44e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb44e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb44e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cb44e-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb44e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cb44e-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="cb44e-134">End of client support</span></span><br/>    | <span data-ttu-id="cb44e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb44e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cb44e-136">Producto</span><span class="sxs-lookup"><span data-stu-id="cb44e-136">Product</span></span><br/>                  | <span data-ttu-id="cb44e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cb44e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cb44e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb44e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb44e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb44e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cb44e-140">IID</span><span class="sxs-lookup"><span data-stu-id="cb44e-140">IID</span></span><br/>                      | <span data-ttu-id="cb44e-141">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="cb44e-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="cb44e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb44e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb44e-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="cb44e-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

