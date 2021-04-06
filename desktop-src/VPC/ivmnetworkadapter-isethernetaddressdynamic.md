---
title: Propiedad IVMNetworkAdapter IsEthernetAddressDynamic (VPCCOMInterfaces. h)
description: Determina si la dirección Ethernet se genera dinámicamente.
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- Propiedad IsEthernetAddressDynamic Virtual PC
- Propiedad IsEthernetAddressDynamic Virtual PC, interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Virtual PC, propiedad IsEthernetAddressDynamic
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078812"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a><span data-ttu-id="7ddb5-106">IVMNetworkAdapter:: IsEthernetAddressDynamic (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7ddb5-106">IVMNetworkAdapter::IsEthernetAddressDynamic property</span></span>

<span data-ttu-id="7ddb5-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7ddb5-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7ddb5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7ddb5-109">Determina si la dirección Ethernet se genera dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-109">Determines whether the Ethernet address is dynamically generated.</span></span>

<span data-ttu-id="7ddb5-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ddb5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ddb5-111">Syntax</span></span>


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a><span data-ttu-id="7ddb5-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7ddb5-112">Property value</span></span>

<span data-ttu-id="7ddb5-113">Establézcalo en VARIANT \_ true si la dirección Ethernet se debe generar dinámicamente y Variant \_ false si la dirección Ethernet es estática.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-113">Set to VARIANT\_TRUE if the Ethernet address should be dynamically generated and VARIANT\_FALSE if the Ethernet address is static.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7ddb5-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7ddb5-114">Error codes</span></span>



| <span data-ttu-id="7ddb5-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="7ddb5-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7ddb5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7ddb5-116">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ddb5-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7ddb5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7ddb5-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-118">The operation was successful.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="7ddb5-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7ddb5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7ddb5-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="7ddb5-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7ddb5-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="7ddb5-122">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-122">The virtual machine was not found.</span></span> <span data-ttu-id="7ddb5-123">Esto puede ocurrir si se quitó el equipo después de crear el objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="7ddb5-123">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/> |
| <dl> <span data-ttu-id="7ddb5-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7ddb5-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7ddb5-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-125">An unexpected error has occurred.</span></span><br/>                                                                                                                         |



## <a name="remarks"></a><span data-ttu-id="7ddb5-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ddb5-126">Remarks</span></span>

<span data-ttu-id="7ddb5-127">Esta propiedad debe establecerse en **true** (valor predeterminado) en la mayoría de las interfaces de red virtual.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-127">This property should be set to **TRUE** (default) for most virtual network interfaces.</span></span> <span data-ttu-id="7ddb5-128">Si el software del invitado requiere una dirección Ethernet estática, esta propiedad debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="7ddb5-128">If software in the guest requires a static Ethernet address, this property should be set to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ddb5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ddb5-129">Requirements</span></span>



| <span data-ttu-id="7ddb5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ddb5-130">Requirement</span></span> | <span data-ttu-id="7ddb5-131">Value</span><span class="sxs-lookup"><span data-stu-id="7ddb5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddb5-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ddb5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7ddb5-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ddb5-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ddb5-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ddb5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7ddb5-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7ddb5-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7ddb5-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7ddb5-136">End of client support</span></span><br/>    | <span data-ttu-id="7ddb5-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ddb5-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7ddb5-138">Producto</span><span class="sxs-lookup"><span data-stu-id="7ddb5-138">Product</span></span><br/>                  | <span data-ttu-id="7ddb5-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7ddb5-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7ddb5-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ddb5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ddb5-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ddb5-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7ddb5-142">IID</span><span class="sxs-lookup"><span data-stu-id="7ddb5-142">IID</span></span><br/>                      | <span data-ttu-id="7ddb5-143">IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="7ddb5-143">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7ddb5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ddb5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ddb5-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="7ddb5-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

