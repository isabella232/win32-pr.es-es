---
title: Propiedad IVMGuestOS IsHostTimeSyncEnabled (VPCCOMInterfaces. h)
description: Indica si los componentes de integración de esta máquina virtual deben sincronizar el reloj del invitado con el reloj del host.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- Propiedad IsHostTimeSyncEnabled Virtual PC
- Propiedad IsHostTimeSyncEnabled Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad IsHostTimeSyncEnabled
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87afddb2e3bc940c5dba7e2548e4355d36142012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651396"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a><span data-ttu-id="0b46e-106">IVMGuestOS:: IsHostTimeSyncEnabled (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0b46e-106">IVMGuestOS::IsHostTimeSyncEnabled property</span></span>

<span data-ttu-id="0b46e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0b46e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0b46e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0b46e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0b46e-109">Indica si los componentes de integración de esta máquina virtual (VM) deben sincronizar el reloj del invitado con el reloj del host.</span><span class="sxs-lookup"><span data-stu-id="0b46e-109">Indicates whether the Integration Components in this virtual machine (VM) should synchronize the guest's clock with the host's clock.</span></span>

<span data-ttu-id="0b46e-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0b46e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b46e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b46e-111">Syntax</span></span>


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="0b46e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0b46e-112">Property value</span></span>

<span data-ttu-id="0b46e-113">Use **Variant \_ true** si los componentes de integración de esta máquina virtual deben sincronizar el reloj del invitado con el reloj del host y la **variante \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0b46e-113">Use **VARIANT\_TRUE** if the integration components in this VM should synchronize the guest's clock with the host's clock and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b46e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0b46e-114">Error codes</span></span>



| <span data-ttu-id="0b46e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="0b46e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0b46e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0b46e-116">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="0b46e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0b46e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0b46e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b46e-118">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="0b46e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0b46e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0b46e-120">No se ha especificado el parámetro *IsEnabled* .</span><span class="sxs-lookup"><span data-stu-id="0b46e-120">The *isEnabled* parameter is not specified.</span></span><br/> |
| <dl> <span data-ttu-id="0b46e-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0b46e-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="0b46e-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="0b46e-122">The configuration is unknown.</span></span><br/>               |
| <dl> <span data-ttu-id="0b46e-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0b46e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0b46e-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0b46e-124">An unexpected error has occurred.</span></span><br/>           |



## <a name="remarks"></a><span data-ttu-id="0b46e-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b46e-125">Remarks</span></span>

<span data-ttu-id="0b46e-126">No se puede cambiar esta configuración mientras la máquina virtual esté activa (es decir, en ejecución o en estado guardado).</span><span class="sxs-lookup"><span data-stu-id="0b46e-126">You cannot change this setting while the virtual machine is active (that is, running or in saved state).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b46e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b46e-127">Requirements</span></span>



| <span data-ttu-id="0b46e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b46e-128">Requirement</span></span> | <span data-ttu-id="0b46e-129">Value</span><span class="sxs-lookup"><span data-stu-id="0b46e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b46e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b46e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0b46e-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b46e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b46e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b46e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0b46e-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0b46e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0b46e-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0b46e-134">End of client support</span></span><br/>    | <span data-ttu-id="0b46e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b46e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0b46e-136">Producto</span><span class="sxs-lookup"><span data-stu-id="0b46e-136">Product</span></span><br/>                  | <span data-ttu-id="0b46e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b46e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0b46e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b46e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b46e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b46e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0b46e-140">IID</span><span class="sxs-lookup"><span data-stu-id="0b46e-140">IID</span></span><br/>                      | <span data-ttu-id="0b46e-141">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="0b46e-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0b46e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b46e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b46e-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="0b46e-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

