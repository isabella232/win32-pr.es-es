---
title: Métodos de la propiedad IADsDNWithString (iAds. h)
description: El método Property de la interfaz IADsDNWithString establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsDNWithString ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa63a933a6a41eec9e6e55906a940cee650c87b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658308"
---
# <a name="iadsdnwithstring-property-methods"></a><span data-ttu-id="e0a95-105">Métodos de propiedad IADsDNWithString</span><span class="sxs-lookup"><span data-stu-id="e0a95-105">IADsDNWithString Property Methods</span></span>

<span data-ttu-id="e0a95-106">El método Property de la interfaz [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0a95-106">The property method of the [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) interface sets the property described in the following table.</span></span> <span data-ttu-id="e0a95-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="e0a95-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e0a95-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e0a95-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="e0a95-109">**DNString**</span><span class="sxs-lookup"><span data-stu-id="e0a95-109">**DNString**</span></span>
<span data-ttu-id="e0a95-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e0a95-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="e0a95-111">Cadena DN asociada a un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="e0a95-111">The DN string associated with a string value.</span></span>

<dt>

<span data-ttu-id="e0a95-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e0a95-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e0a95-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e0a95-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0a95-114">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="e0a95-114">**StringValue**</span></span>
<span data-ttu-id="e0a95-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e0a95-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="e0a95-116">Valor de cadena asociado a un DN de un objeto.</span><span class="sxs-lookup"><span data-stu-id="e0a95-116">The string value associated with a DN of an object.</span></span>

<dt>

<span data-ttu-id="e0a95-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e0a95-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e0a95-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e0a95-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="e0a95-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0a95-119">Requirements</span></span>



| <span data-ttu-id="e0a95-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a95-120">Requirement</span></span> | <span data-ttu-id="e0a95-121">Value</span><span class="sxs-lookup"><span data-stu-id="e0a95-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a95-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0a95-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e0a95-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0a95-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0a95-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0a95-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e0a95-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0a95-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0a95-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0a95-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0a95-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0a95-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="e0a95-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0a95-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0a95-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0a95-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0a95-130">IID</span><span class="sxs-lookup"><span data-stu-id="e0a95-130">IID</span></span><br/>                      | <span data-ttu-id="e0a95-131">IID \_ IADsDNWithString se define como 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="e0a95-131">IID\_IADsDNWithString is defined as 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="e0a95-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0a95-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a95-133">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="e0a95-133">**IADsDNWithString**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[<span data-ttu-id="e0a95-134">**\_DN \_ de ADS con \_ cadena**</span><span class="sxs-lookup"><span data-stu-id="e0a95-134">**ADS\_DN\_WITH\_STRING**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 





