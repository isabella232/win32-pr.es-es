---
title: Métodos de la propiedad IADsTypedName (iAds. h)
description: El método Property de la interfaz IADsTypedName establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsTypedName ADSI
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656527"
---
# <a name="iadstypedname-property-methods"></a><span data-ttu-id="30855-105">Métodos de propiedad IADsTypedName</span><span class="sxs-lookup"><span data-stu-id="30855-105">IADsTypedName Property Methods</span></span>

<span data-ttu-id="30855-106">El método Property de la interfaz [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="30855-106">The property method of the [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) interface sets the property described in the following table.</span></span> <span data-ttu-id="30855-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="30855-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="30855-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30855-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="30855-109">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="30855-109">**Interval**</span></span>
<span data-ttu-id="30855-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="30855-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="30855-111">Frecuencia de referencia del objeto.</span><span class="sxs-lookup"><span data-stu-id="30855-111">The frequency of reference of the object.</span></span>

<dt>

<span data-ttu-id="30855-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="30855-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="30855-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="30855-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="30855-114">**Level**</span><span class="sxs-lookup"><span data-stu-id="30855-114">**Level**</span></span>
<span data-ttu-id="30855-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="30855-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="30855-116">Nivel de prioridad asociado al objeto.</span><span class="sxs-lookup"><span data-stu-id="30855-116">The priority level associated with the object.</span></span>

<dt>

<span data-ttu-id="30855-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="30855-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="30855-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="30855-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="30855-119">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="30855-119">**ObjectName**</span></span>
<span data-ttu-id="30855-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="30855-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="30855-121">Nombre de un objeto.</span><span class="sxs-lookup"><span data-stu-id="30855-121">The name of an object.</span></span>

<dt>

<span data-ttu-id="30855-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="30855-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="30855-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="30855-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="30855-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30855-124">Requirements</span></span>



| <span data-ttu-id="30855-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="30855-125">Requirement</span></span> | <span data-ttu-id="30855-126">Value</span><span class="sxs-lookup"><span data-stu-id="30855-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30855-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30855-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30855-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30855-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30855-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30855-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30855-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30855-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30855-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30855-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="30855-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="30855-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="30855-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30855-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30855-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30855-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="30855-135">IID</span><span class="sxs-lookup"><span data-stu-id="30855-135">IID</span></span><br/>                      | <span data-ttu-id="30855-136">IID \_ IADsTypedName se define como B371A349-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="30855-136">IID\_IADsTypedName is defined as B371A349-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="30855-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="30855-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30855-138">**IADsTypedName**</span><span class="sxs-lookup"><span data-stu-id="30855-138">**IADsTypedName**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[<span data-ttu-id="30855-139">**\_TYPEDNAME ADS**</span><span class="sxs-lookup"><span data-stu-id="30855-139">**ADS\_TYPEDNAME**</span></span>](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 





