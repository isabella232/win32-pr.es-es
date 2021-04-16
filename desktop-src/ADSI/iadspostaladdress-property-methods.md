---
title: Métodos de la propiedad IADsPostalAddress (iAds. h)
description: El método Property de la interfaz IADsPostalAddress establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPostalAddress ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d8eeaac8fa258a2df1452b8aa261ee59b3cc85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658297"
---
# <a name="iadspostaladdress-property-methods"></a><span data-ttu-id="9cd8b-105">Métodos de propiedad IADsPostalAddress</span><span class="sxs-lookup"><span data-stu-id="9cd8b-105">IADsPostalAddress Property Methods</span></span>

<span data-ttu-id="9cd8b-106">El método Property de la interfaz [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9cd8b-106">The property method of the [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) interface sets the property described in the following table.</span></span> <span data-ttu-id="9cd8b-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9cd8b-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9cd8b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9cd8b-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9cd8b-109">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="9cd8b-109">**PostalAddress**</span></span>
<span data-ttu-id="9cd8b-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9cd8b-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="9cd8b-111">Una matriz de seis cadenas que contienen la dirección postal del usuario.</span><span class="sxs-lookup"><span data-stu-id="9cd8b-111">An array of six strings holding the postal address of the user.</span></span>

<dt>

<span data-ttu-id="9cd8b-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9cd8b-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9cd8b-113">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="9cd8b-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="9cd8b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cd8b-114">Requirements</span></span>



| <span data-ttu-id="9cd8b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd8b-115">Requirement</span></span> | <span data-ttu-id="9cd8b-116">Value</span><span class="sxs-lookup"><span data-stu-id="9cd8b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd8b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cd8b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd8b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cd8b-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cd8b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cd8b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd8b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cd8b-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cd8b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cd8b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cd8b-122"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cd8b-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="9cd8b-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9cd8b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cd8b-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cd8b-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="9cd8b-125">IID</span><span class="sxs-lookup"><span data-stu-id="9cd8b-125">IID</span></span><br/>                      | <span data-ttu-id="9cd8b-126">IID \_ IADsPostalAddress se define como 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="9cd8b-126">IID\_IADsPostalAddress is defined as 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="9cd8b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cd8b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd8b-128">**IADsPostalAddress**</span><span class="sxs-lookup"><span data-stu-id="9cd8b-128">**IADsPostalAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[<span data-ttu-id="9cd8b-129">**\_POSTALADDRESS ADS**</span><span class="sxs-lookup"><span data-stu-id="9cd8b-129">**ADS\_POSTALADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 





