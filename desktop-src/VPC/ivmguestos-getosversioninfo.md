---
title: Método IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces. h)
description: Recupera información de versión del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Método GetOsVersionInfo Virtual PC
- Método GetOsVersionInfo Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676951"
---
# <a name="ivmguestosgetosversioninfo-method"></a><span data-ttu-id="4a5b8-106">IVMGuestOS:: GetOsVersionInfo (método)</span><span class="sxs-lookup"><span data-stu-id="4a5b8-106">IVMGuestOS::GetOsVersionInfo method</span></span>

<span data-ttu-id="4a5b8-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4a5b8-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4a5b8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4a5b8-109">Recupera información de versión del sistema operativo invitado que se ejecuta en la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="4a5b8-109">Retrieves version information for the guest operating system running in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a5b8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a5b8-110">Syntax</span></span>


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4a5b8-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a5b8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a5b8-112">*guestOsVersionInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4a5b8-112">*guestOsVersionInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-113">Puntero a una estructura [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) .</span><span class="sxs-lookup"><span data-stu-id="4a5b8-113">A pointer to a [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a5b8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a5b8-114">Return value</span></span>

<span data-ttu-id="4a5b8-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4a5b8-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a5b8-116">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="4a5b8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a5b8-117">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a5b8-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="4a5b8-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="4a5b8-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="4a5b8-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4a5b8-122"><dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="4a5b8-123">No hay suficiente memoria disponible para completar esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-123">There is not enough memory available to complete this request.</span></span><br/> |
| <dl> <span data-ttu-id="4a5b8-124"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="4a5b8-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-125">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="4a5b8-126"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="4a5b8-127">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-127">The VM is not running.</span></span><br/>                                         |
| <dl> <span data-ttu-id="4a5b8-128"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="4a5b8-129">Los componentes de integración no están instalados en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-129">Integration components are not installed in this VM.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="4a5b8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a5b8-130">Requirements</span></span>



| <span data-ttu-id="4a5b8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a5b8-131">Requirement</span></span> | <span data-ttu-id="4a5b8-132">Value</span><span class="sxs-lookup"><span data-stu-id="4a5b8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a5b8-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a5b8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4a5b8-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a5b8-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a5b8-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a5b8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4a5b8-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4a5b8-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4a5b8-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4a5b8-137">End of client support</span></span><br/>    | <span data-ttu-id="4a5b8-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4a5b8-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4a5b8-139">Producto</span><span class="sxs-lookup"><span data-stu-id="4a5b8-139">Product</span></span><br/>                  | <span data-ttu-id="4a5b8-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4a5b8-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4a5b8-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a5b8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a5b8-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4a5b8-143">IID</span><span class="sxs-lookup"><span data-stu-id="4a5b8-143">IID</span></span><br/>                      | <span data-ttu-id="4a5b8-144">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="4a5b8-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4a5b8-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a5b8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a5b8-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

