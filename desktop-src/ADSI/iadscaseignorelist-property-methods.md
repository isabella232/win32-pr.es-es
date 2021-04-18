---
title: Métodos de la propiedad IADsCaseIgnoreList (iAds. h)
description: El método Property de la interfaz IADsCaseIgnoreList establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsCaseIgnoreList ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aabf26508c3e38e117ad25721af8bece5d69b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658310"
---
# <a name="iadscaseignorelist-property-methods"></a><span data-ttu-id="ef451-105">Métodos de propiedad IADsCaseIgnoreList</span><span class="sxs-lookup"><span data-stu-id="ef451-105">IADsCaseIgnoreList Property Methods</span></span>

<span data-ttu-id="ef451-106">El método Property de la interfaz [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ef451-106">The property method of the [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) interface sets the property described in the following table.</span></span> <span data-ttu-id="ef451-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ef451-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ef451-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef451-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ef451-109">**CaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="ef451-109">**CaseIgnoreList**</span></span>
<span data-ttu-id="ef451-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ef451-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ef451-111">Secuencia ordenada de cadenas que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ef451-111">An ordered sequence of case insensitive strings.</span></span>

<dt>

<span data-ttu-id="ef451-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ef451-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ef451-113">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="ef451-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="ef451-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef451-114">Requirements</span></span>



| <span data-ttu-id="ef451-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef451-115">Requirement</span></span> | <span data-ttu-id="ef451-116">Value</span><span class="sxs-lookup"><span data-stu-id="ef451-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef451-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef451-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ef451-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef451-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef451-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef451-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ef451-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef451-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef451-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef451-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef451-122"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef451-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ef451-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef451-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef451-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef451-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef451-125">IID</span><span class="sxs-lookup"><span data-stu-id="ef451-125">IID</span></span><br/>                      | <span data-ttu-id="ef451-126">IID \_ IADsCaseIgnoreList se define como 7B66B533-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="ef451-126">IID\_IADsCaseIgnoreList is defined as 7B66B533-4680-11D1-A3B4-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="ef451-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef451-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef451-128">**IADsCaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="ef451-128">**IADsCaseIgnoreList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[<span data-ttu-id="ef451-129">**\_lista CASEIGNORE \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="ef451-129">**ADS\_CASEIGNORE\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





