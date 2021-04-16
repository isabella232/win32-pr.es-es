---
title: Métodos de la propiedad IADsFaxNumber (iAds. h)
description: El método Property de la interfaz IADsFaxNumber establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsFaxNumber ADSI
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658305"
---
# <a name="iadsfaxnumber-property-methods"></a><span data-ttu-id="6f251-105">Métodos de propiedad IADsFaxNumber</span><span class="sxs-lookup"><span data-stu-id="6f251-105">IADsFaxNumber Property Methods</span></span>

<span data-ttu-id="6f251-106">El método Property de la interfaz [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6f251-106">The property method of the [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) interface sets the property described in the following table.</span></span> <span data-ttu-id="6f251-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6f251-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6f251-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f251-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6f251-109">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f251-109">**Parameters**</span></span>
<span data-ttu-id="6f251-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f251-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f251-111">Los parámetros del equipo de fax.</span><span class="sxs-lookup"><span data-stu-id="6f251-111">The parameters for the fax machine.</span></span>

<dt>

<span data-ttu-id="6f251-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f251-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6f251-113">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="6f251-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f251-114">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="6f251-114">**TelephoneNumber**</span></span>
<span data-ttu-id="6f251-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f251-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f251-116">Número de teléfono del equipo de fax.</span><span class="sxs-lookup"><span data-stu-id="6f251-116">The telephone number of the fax machine.</span></span>

<dt>

<span data-ttu-id="6f251-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f251-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6f251-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f251-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="6f251-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f251-119">Requirements</span></span>



| <span data-ttu-id="6f251-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f251-120">Requirement</span></span> | <span data-ttu-id="6f251-121">Value</span><span class="sxs-lookup"><span data-stu-id="6f251-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f251-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f251-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6f251-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f251-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f251-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f251-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6f251-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f251-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f251-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f251-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f251-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f251-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6f251-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f251-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f251-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f251-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f251-130">IID</span><span class="sxs-lookup"><span data-stu-id="6f251-130">IID</span></span><br/>                      | <span data-ttu-id="6f251-131">IID \_ IADsFaxNumber se define como A910DEA9-4680-11D1-0A3B-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="6f251-131">IID\_IADsFaxNumber is defined as A910DEA9-4680-11D1-0A3B-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6f251-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f251-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f251-133">**IADsFaxNumber**</span><span class="sxs-lookup"><span data-stu-id="6f251-133">**IADsFaxNumber**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[<span data-ttu-id="6f251-134">**\_FAXNUMBER ADS**</span><span class="sxs-lookup"><span data-stu-id="6f251-134">**ADS\_FAXNUMBER**</span></span>](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 





