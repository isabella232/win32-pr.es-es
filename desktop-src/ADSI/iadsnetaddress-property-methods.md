---
title: Métodos de la propiedad IADsNetAddress (iAds. h)
description: El método Property de la interfaz IADsNetAddress establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsNetAddress ADSI
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073033c703db8eaa55b05058d6d2bbc3d3167f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803169"
---
# <a name="iadsnetaddress-property-methods"></a><span data-ttu-id="8bfe9-105">Métodos de propiedad IADsNetAddress</span><span class="sxs-lookup"><span data-stu-id="8bfe9-105">IADsNetAddress Property Methods</span></span>

<span data-ttu-id="8bfe9-106">El método Property de la interfaz [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8bfe9-106">The property method of the [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) interface sets the property described in the following table.</span></span> <span data-ttu-id="8bfe9-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8bfe9-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8bfe9-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bfe9-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="8bfe9-109">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="8bfe9-109">**Address**</span></span>
<span data-ttu-id="8bfe9-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8bfe9-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="8bfe9-111">Una dirección de red.</span><span class="sxs-lookup"><span data-stu-id="8bfe9-111">A network address.</span></span>

<dt>

<span data-ttu-id="8bfe9-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8bfe9-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8bfe9-113">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="8bfe9-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8bfe9-114">**AddressType**</span><span class="sxs-lookup"><span data-stu-id="8bfe9-114">**AddressType**</span></span>
<span data-ttu-id="8bfe9-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8bfe9-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="8bfe9-116">Un tipo de protocolos de comunicación.</span><span class="sxs-lookup"><span data-stu-id="8bfe9-116">A type of communication protocols.</span></span>

<dt>

<span data-ttu-id="8bfe9-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8bfe9-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8bfe9-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="8bfe9-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="8bfe9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bfe9-119">Requirements</span></span>



| <span data-ttu-id="8bfe9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bfe9-120">Requirement</span></span> | <span data-ttu-id="8bfe9-121">Value</span><span class="sxs-lookup"><span data-stu-id="8bfe9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bfe9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bfe9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8bfe9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bfe9-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8bfe9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bfe9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8bfe9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bfe9-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8bfe9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bfe9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bfe9-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bfe9-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="8bfe9-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8bfe9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bfe9-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bfe9-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="8bfe9-130">IID</span><span class="sxs-lookup"><span data-stu-id="8bfe9-130">IID</span></span><br/>                      | <span data-ttu-id="8bfe9-131">IID \_ IADsNetAddress se define como B21A50A9-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="8bfe9-131">IID\_IADsNetAddress is defined as B21A50A9-4080-11D1-A3AC-00C04FB950DC</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8bfe9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bfe9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfe9-133">**IADsNetAddress**</span><span class="sxs-lookup"><span data-stu-id="8bfe9-133">**IADsNetAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[<span data-ttu-id="8bfe9-134">**\_NETADDRESS ADS**</span><span class="sxs-lookup"><span data-stu-id="8bfe9-134">**ADS\_NETADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 





