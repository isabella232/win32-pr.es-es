---
title: Métodos de la propiedad IADsTimestamp (iAds. h)
description: El método Property de la interfaz IADsTimestamp establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsTimestamp ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490240"
---
# <a name="iadstimestamp-property-methods"></a><span data-ttu-id="aee8a-105">Métodos de propiedad IADsTimestamp</span><span class="sxs-lookup"><span data-stu-id="aee8a-105">IADsTimestamp Property Methods</span></span>

<span data-ttu-id="aee8a-106">El método Property de la interfaz [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="aee8a-106">The property method of the [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) interface sets the property described in the following table.</span></span> <span data-ttu-id="aee8a-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="aee8a-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="aee8a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aee8a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="aee8a-109">**Id. de evento**</span><span class="sxs-lookup"><span data-stu-id="aee8a-109">**EventID**</span></span>
<span data-ttu-id="aee8a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aee8a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="aee8a-111">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="aee8a-111">An event identifier.</span></span>

<dt>

<span data-ttu-id="aee8a-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="aee8a-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aee8a-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="aee8a-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aee8a-114">**WholeSeconds**</span><span class="sxs-lookup"><span data-stu-id="aee8a-114">**WholeSeconds**</span></span>
<span data-ttu-id="aee8a-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aee8a-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="aee8a-116">Número de segundos con un valor de cero 12:00 AM, 1970 de enero de UTC.</span><span class="sxs-lookup"><span data-stu-id="aee8a-116">Number of seconds with zero value being 12:00 AM, January 1970, UTC.</span></span>

<dt>

<span data-ttu-id="aee8a-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="aee8a-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aee8a-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="aee8a-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="aee8a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aee8a-119">Requirements</span></span>



| <span data-ttu-id="aee8a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee8a-120">Requirement</span></span> | <span data-ttu-id="aee8a-121">Value</span><span class="sxs-lookup"><span data-stu-id="aee8a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee8a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aee8a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aee8a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee8a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aee8a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aee8a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aee8a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aee8a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aee8a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aee8a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee8a-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="aee8a-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="aee8a-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aee8a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aee8a-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee8a-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="aee8a-130">IID</span><span class="sxs-lookup"><span data-stu-id="aee8a-130">IID</span></span><br/>                      | <span data-ttu-id="aee8a-131">IID \_ IADsTimestamp se define como B2F5A901-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="aee8a-131">IID\_IADsTimestamp is defined as B2F5A901-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="aee8a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="aee8a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee8a-133">**IADsTimestamp**</span><span class="sxs-lookup"><span data-stu-id="aee8a-133">**IADsTimestamp**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[<span data-ttu-id="aee8a-134">**marca de tiempo de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="aee8a-134">**ADS\_TIMESTAMP**</span></span>](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





