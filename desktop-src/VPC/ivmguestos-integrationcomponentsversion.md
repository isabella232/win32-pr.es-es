---
title: Propiedad IVMGuestOS IntegrationComponentsVersion (VPCCOMInterfaces. h)
description: Recupera la versión de los componentes de integración instalados en el sistema operativo invitado.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- Propiedad IntegrationComponentsVersion Virtual PC
- Propiedad IntegrationComponentsVersion Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad IntegrationComponentsVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85352614b89ab208377fe44fe3b970c693d60dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801274"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a><span data-ttu-id="f0852-106">IVMGuestOS:: IntegrationComponentsVersion (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f0852-106">IVMGuestOS::IntegrationComponentsVersion property</span></span>

<span data-ttu-id="f0852-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0852-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f0852-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0852-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f0852-109">Recupera la versión de los componentes de integración instalados en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="f0852-109">Retrieves the version of the Integration Components installed in the guest operating system.</span></span>

<span data-ttu-id="f0852-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f0852-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0852-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0852-111">Syntax</span></span>


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a><span data-ttu-id="f0852-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f0852-112">Property value</span></span>

<span data-ttu-id="f0852-113">La versión.</span><span class="sxs-lookup"><span data-stu-id="f0852-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0852-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f0852-114">Error codes</span></span>



| <span data-ttu-id="f0852-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="f0852-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="f0852-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f0852-116">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0852-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f0852-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="f0852-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0852-118">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="f0852-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f0852-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="f0852-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f0852-120">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f0852-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f0852-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="f0852-122">No se encontró la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="f0852-122">The virtual machine (VM) could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f0852-123"><dt>Máquina virtual \_ E/s \_ \_ no \_ DISP</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="f0852-123"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="f0852-124">Los componentes de integración no están instalados en esta máquina virtual o la máquina virtual no se ha iniciado nunca.</span><span class="sxs-lookup"><span data-stu-id="f0852-124">Integration Components are not installed in this VM, or the VM was never started.</span></span><br/> |
| <dl> <span data-ttu-id="f0852-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f0852-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="f0852-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f0852-126">An unexpected error has occurred.</span></span><br/>                                                 |



## <a name="requirements"></a><span data-ttu-id="f0852-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0852-127">Requirements</span></span>



| <span data-ttu-id="f0852-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0852-128">Requirement</span></span> | <span data-ttu-id="f0852-129">Value</span><span class="sxs-lookup"><span data-stu-id="f0852-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0852-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0852-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f0852-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0852-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0852-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0852-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f0852-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0852-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f0852-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f0852-134">End of client support</span></span><br/>    | <span data-ttu-id="f0852-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0852-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f0852-136">Producto</span><span class="sxs-lookup"><span data-stu-id="f0852-136">Product</span></span><br/>                  | <span data-ttu-id="f0852-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f0852-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f0852-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0852-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0852-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0852-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f0852-140">IID</span><span class="sxs-lookup"><span data-stu-id="f0852-140">IID</span></span><br/>                      | <span data-ttu-id="f0852-141">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="f0852-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f0852-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0852-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0852-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="f0852-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

