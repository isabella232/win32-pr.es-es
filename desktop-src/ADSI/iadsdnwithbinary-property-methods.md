---
title: Métodos de la propiedad IADsDNWithBinary (iAds. h)
description: El método Property de la interfaz IADsDNWithBinary establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsDNWithBinary ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150775"
---
# <a name="iadsdnwithbinary-property-methods"></a><span data-ttu-id="82c5f-105">Métodos de propiedad IADsDNWithBinary</span><span class="sxs-lookup"><span data-stu-id="82c5f-105">IADsDNWithBinary Property Methods</span></span>

<span data-ttu-id="82c5f-106">El método Property de la interfaz [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="82c5f-106">The property method of the [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) interface sets the property described in the following table.</span></span> <span data-ttu-id="82c5f-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="82c5f-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="82c5f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82c5f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="82c5f-109">**BinaryValue**</span><span class="sxs-lookup"><span data-stu-id="82c5f-109">**BinaryValue**</span></span>
<span data-ttu-id="82c5f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="82c5f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="82c5f-111">GUID de un objeto asociado a un DN.</span><span class="sxs-lookup"><span data-stu-id="82c5f-111">The GUID of an object associated with a DN.</span></span>

<dt>

<span data-ttu-id="82c5f-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82c5f-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="82c5f-113">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="82c5f-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="82c5f-114">**DNString**</span><span class="sxs-lookup"><span data-stu-id="82c5f-114">**DNString**</span></span>
<span data-ttu-id="82c5f-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="82c5f-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="82c5f-116">Cadena DN asociada al GUID de un objeto.</span><span class="sxs-lookup"><span data-stu-id="82c5f-116">The DN string associated with the GUID of an object.</span></span>

<dt>

<span data-ttu-id="82c5f-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82c5f-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="82c5f-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="82c5f-118">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="82c5f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82c5f-119">Requirements</span></span>



| <span data-ttu-id="82c5f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="82c5f-120">Requirement</span></span> | <span data-ttu-id="82c5f-121">Value</span><span class="sxs-lookup"><span data-stu-id="82c5f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82c5f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82c5f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="82c5f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82c5f-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82c5f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82c5f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="82c5f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82c5f-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82c5f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82c5f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="82c5f-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="82c5f-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="82c5f-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82c5f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82c5f-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82c5f-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="82c5f-130">IID</span><span class="sxs-lookup"><span data-stu-id="82c5f-130">IID</span></span><br/>                      | <span data-ttu-id="82c5f-131">IID \_ IADsDNWithBinary se define como 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="82c5f-131">IID\_IADsDNWithBinary is defined as 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="82c5f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="82c5f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c5f-133">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="82c5f-133">**IADsDNWithBinary**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[<span data-ttu-id="82c5f-134">**\_DN \_ de ADS con \_ binario**</span><span class="sxs-lookup"><span data-stu-id="82c5f-134">**ADS\_DN\_WITH\_BINARY**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 





