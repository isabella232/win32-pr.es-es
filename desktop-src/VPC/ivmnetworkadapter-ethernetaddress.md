---
title: Propiedad IVMNetworkAdapter denominaba ethernetaddress (VPCCOMInterfaces. h)
description: Dirección Ethernet (MAC) de la interfaz de red.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Propiedad denominaba ethernetaddress Virtual PC
- Propiedad denominaba ethernetaddress Virtual PC, interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Virtual PC, propiedad denominaba ethernetaddress
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800968"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a><span data-ttu-id="f5556-106">IVMNetworkAdapter:: denominaba ethernetaddress (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f5556-106">IVMNetworkAdapter::EthernetAddress property</span></span>

<span data-ttu-id="f5556-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5556-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f5556-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f5556-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f5556-109">Recupera y establece la dirección Ethernet (MAC) de la interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="f5556-109">Retrieves and sets the Ethernet (MAC) address of the network interface.</span></span>

<span data-ttu-id="f5556-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f5556-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5556-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5556-111">Syntax</span></span>


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a><span data-ttu-id="f5556-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f5556-112">Property value</span></span>

<span data-ttu-id="f5556-113">La dirección MAC de la NIC virtual.</span><span class="sxs-lookup"><span data-stu-id="f5556-113">The MAC address of the virtual NIC.</span></span> <span data-ttu-id="f5556-114">Debe tener el formato "*XX* - *XX* XX XX XX XX", -  -  -  - donde cada *X* es un dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="f5556-114">It should have the form "*XX*-*XX*-*XX*-*XX*-*XX*-*XX*" where each *X* is a hexadecimal digit.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f5556-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f5556-115">Error codes</span></span>



| <span data-ttu-id="f5556-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="f5556-116">Name/value</span></span>                                                                                                                                                                         | <span data-ttu-id="f5556-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f5556-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5556-118"><dt>S \_ correcto</dt></span><span class="sxs-lookup"><span data-stu-id="f5556-118"><dt>S\_OK</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="f5556-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f5556-119">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="f5556-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f5556-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                              | <span data-ttu-id="f5556-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f5556-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="f5556-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f5556-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                           | <span data-ttu-id="f5556-123">El parámetro no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="f5556-123">The parameter is not in the correct format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="f5556-124"><dt>Máquina virtual \_ E no se pudo \_ \_ establecer la \_ \_ \_ dirección Mac dinámica</dt> <dt>0xA004070A</dt></span><span class="sxs-lookup"><span data-stu-id="f5556-124"><dt>VM\_E\_CANT\_SET\_DYNAMIC\_MAC\_ADDRESS</dt> <dt>0xA004070A</dt></span></span> </dl> | <span data-ttu-id="f5556-125">La dirección Ethernet de una interfaz de red se puede generar dinámicamente, o bien el usuario puede establecerla en una dirección estática.</span><span class="sxs-lookup"><span data-stu-id="f5556-125">The Ethernet address for a network interface can either be generated dynamically or can be set to a static address by the user.</span></span> <span data-ttu-id="f5556-126">No se puede llamar a este método cuando se establece la dirección para que se genere dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="f5556-126">This method cannot be called when the address is set to be generated dynamically.</span></span> <span data-ttu-id="f5556-127">La propiedad [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) se usa para cambiar el comportamiento de generación de la dirección Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f5556-127">The [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) property is used to change the generation behavior of the Ethernet address.</span></span><br/> |
| <dl> <span data-ttu-id="f5556-128"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5556-128"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                      | <span data-ttu-id="f5556-129">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5556-129">The virtual machine was not found.</span></span> <span data-ttu-id="f5556-130">Esto puede ocurrir si se quitó el equipo después de crear el objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="f5556-130">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="f5556-131"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f5556-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                      | <span data-ttu-id="f5556-132">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f5556-132">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="f5556-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5556-133">Requirements</span></span>



| <span data-ttu-id="f5556-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5556-134">Requirement</span></span> | <span data-ttu-id="f5556-135">Value</span><span class="sxs-lookup"><span data-stu-id="f5556-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5556-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5556-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f5556-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5556-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5556-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5556-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f5556-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f5556-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f5556-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f5556-140">End of client support</span></span><br/>    | <span data-ttu-id="f5556-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5556-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f5556-142">Producto</span><span class="sxs-lookup"><span data-stu-id="f5556-142">Product</span></span><br/>                  | <span data-ttu-id="f5556-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f5556-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f5556-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5556-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5556-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5556-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f5556-146">IID</span><span class="sxs-lookup"><span data-stu-id="f5556-146">IID</span></span><br/>                      | <span data-ttu-id="f5556-147">IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="f5556-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f5556-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5556-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5556-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="f5556-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

