---
title: Métodos de la propiedad IADsOctetList (iAds. h)
description: El método Property de la interfaz IADsOctetList establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsOctetList ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3631adaf00cf599214296e1792ffab8697ba5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996830"
---
# <a name="iadsoctetlist-property-methods"></a><span data-ttu-id="83a6f-105">Métodos de propiedad IADsOctetList</span><span class="sxs-lookup"><span data-stu-id="83a6f-105">IADsOctetList Property Methods</span></span>

<span data-ttu-id="83a6f-106">El método Property de la interfaz [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="83a6f-106">The property method of the [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) interface sets the property described in the following table.</span></span> <span data-ttu-id="83a6f-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="83a6f-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="83a6f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83a6f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="83a6f-109">**OctetList**</span><span class="sxs-lookup"><span data-stu-id="83a6f-109">**OctetList**</span></span>
<span data-ttu-id="83a6f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a6f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a6f-111">Secuencia ordenada de matrices de bytes.</span><span class="sxs-lookup"><span data-stu-id="83a6f-111">An ordered sequence of byte arrays.</span></span>

<dt>

<span data-ttu-id="83a6f-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="83a6f-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a6f-113">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="83a6f-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="83a6f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83a6f-114">Requirements</span></span>



| <span data-ttu-id="83a6f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="83a6f-115">Requirement</span></span> | <span data-ttu-id="83a6f-116">Value</span><span class="sxs-lookup"><span data-stu-id="83a6f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83a6f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83a6f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83a6f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83a6f-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83a6f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83a6f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83a6f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83a6f-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83a6f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83a6f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="83a6f-122"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="83a6f-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="83a6f-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83a6f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83a6f-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83a6f-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="83a6f-125">IID</span><span class="sxs-lookup"><span data-stu-id="83a6f-125">IID</span></span><br/>                      | <span data-ttu-id="83a6f-126">IID \_ IADsOctetList se define como 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="83a6f-126">IID\_IADsOctetList is defined as 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="83a6f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="83a6f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a6f-128">**IADsOctetList**</span><span class="sxs-lookup"><span data-stu-id="83a6f-128">**IADsOctetList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[<span data-ttu-id="83a6f-129">**\_lista de octetos de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="83a6f-129">**ADS\_OCTET\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 





