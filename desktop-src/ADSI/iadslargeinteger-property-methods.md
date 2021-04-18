---
title: Métodos de la propiedad IADsLargeInteger (iAds. h)
description: Los métodos de propiedad de la interfaz IADsLargeInteger obtienen y establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsLargeInteger ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097e9ae7387658f983c691e56e4f90ba40dea407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658302"
---
# <a name="iadslargeinteger-property-methods"></a><span data-ttu-id="12caa-105">Métodos de propiedad IADsLargeInteger</span><span class="sxs-lookup"><span data-stu-id="12caa-105">IADsLargeInteger Property Methods</span></span>

<span data-ttu-id="12caa-106">Los métodos de propiedad de la interfaz [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) obtienen y establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="12caa-106">The property methods of the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface get and set the properties described in the following table.</span></span> <span data-ttu-id="12caa-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="12caa-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="12caa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12caa-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="12caa-109">**HighPart**</span><span class="sxs-lookup"><span data-stu-id="12caa-109">**HighPart**</span></span>
<span data-ttu-id="12caa-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12caa-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="12caa-111">Parte alta del entero.</span><span class="sxs-lookup"><span data-stu-id="12caa-111">The high part of the integer.</span></span>

<dt>

<span data-ttu-id="12caa-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12caa-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12caa-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="12caa-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12caa-114">**LowPart**</span><span class="sxs-lookup"><span data-stu-id="12caa-114">**LowPart**</span></span>
<span data-ttu-id="12caa-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12caa-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="12caa-116">Parte baja del entero.</span><span class="sxs-lookup"><span data-stu-id="12caa-116">The low part of the integer.</span></span>

<dt>

<span data-ttu-id="12caa-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12caa-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12caa-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="12caa-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="12caa-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12caa-119">Remarks</span></span>

<span data-ttu-id="12caa-120">Si largeInt es del tipo **LargeInteger** , su valor se especifica mediante los valores de **HighPart** y **LowPart** según la fórmula siguiente.</span><span class="sxs-lookup"><span data-stu-id="12caa-120">If largeInt is of the **LargeInteger** type, its value is specified by those of **HighPart** and **LowPart** according to the following formula.</span></span>


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a><span data-ttu-id="12caa-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="12caa-121">Examples</span></span>

<span data-ttu-id="12caa-122">En el siguiente ejemplo de código de Visual Basic se establece un entero grande en 43937327281.</span><span class="sxs-lookup"><span data-stu-id="12caa-122">The following Visual Basic code example sets a large integer to 43937327281.</span></span>


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a><span data-ttu-id="12caa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12caa-123">Requirements</span></span>



| <span data-ttu-id="12caa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="12caa-124">Requirement</span></span> | <span data-ttu-id="12caa-125">Value</span><span class="sxs-lookup"><span data-stu-id="12caa-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12caa-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12caa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="12caa-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12caa-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12caa-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12caa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="12caa-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12caa-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12caa-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12caa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="12caa-131"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="12caa-131"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="12caa-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12caa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12caa-133"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12caa-133"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="12caa-134">IID</span><span class="sxs-lookup"><span data-stu-id="12caa-134">IID</span></span><br/>                      | <span data-ttu-id="12caa-135">IID \_ IADsLargeInteger se define como 9068270B-0939-11D1-8BE1-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="12caa-135">IID\_IADsLargeInteger is defined as 9068270B-0939-11D1-8BE1-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="12caa-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="12caa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12caa-137">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="12caa-137">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





