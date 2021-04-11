---
title: Métodos de la propiedad IADsHold (iAds. h)
description: El método Property de la interfaz IADsHold establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsHold ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae2499efb461e6c13397fdaef75e515f0a1a21a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150771"
---
# <a name="iadshold-property-methods"></a><span data-ttu-id="3f1a7-105">Métodos de propiedad IADsHold</span><span class="sxs-lookup"><span data-stu-id="3f1a7-105">IADsHold Property Methods</span></span>

<span data-ttu-id="3f1a7-106">El método Property de la interfaz [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3f1a7-106">The property method of the [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) interface sets the property described in the following table.</span></span> <span data-ttu-id="3f1a7-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3f1a7-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3f1a7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f1a7-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3f1a7-109">**Amount**</span><span class="sxs-lookup"><span data-stu-id="3f1a7-109">**Amount**</span></span>
<span data-ttu-id="3f1a7-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3f1a7-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3f1a7-111">La cantidad de cargos aplicados al usuario durante el período en espera mientras el servidor comprueba el saldo de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="3f1a7-111">The amount of charges levied against the user for the period on hold while the server checks the account balance of the user.</span></span>

<dt>

<span data-ttu-id="3f1a7-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f1a7-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f1a7-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="3f1a7-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f1a7-114">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="3f1a7-114">**ObjectName**</span></span>
<span data-ttu-id="3f1a7-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3f1a7-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="3f1a7-116">Nombre del objeto que representa a un usuario en espera.</span><span class="sxs-lookup"><span data-stu-id="3f1a7-116">The name of the object representing a user on hold.</span></span>

<dt>

<span data-ttu-id="3f1a7-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f1a7-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f1a7-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f1a7-118">Scripting data type: **BSTR**</span></span>
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

 

## <a name="requirements"></a><span data-ttu-id="3f1a7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f1a7-119">Requirements</span></span>



| <span data-ttu-id="3f1a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f1a7-120">Requirement</span></span> | <span data-ttu-id="3f1a7-121">Value</span><span class="sxs-lookup"><span data-stu-id="3f1a7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f1a7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f1a7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3f1a7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f1a7-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3f1a7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f1a7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3f1a7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f1a7-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3f1a7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f1a7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f1a7-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f1a7-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3f1a7-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f1a7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f1a7-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f1a7-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f1a7-130">IID</span><span class="sxs-lookup"><span data-stu-id="3f1a7-130">IID</span></span><br/>                      | <span data-ttu-id="3f1a7-131">IID \_ IADsHold se define como B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="3f1a7-131">IID\_IADsHold is defined as B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3f1a7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f1a7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f1a7-133">**IADsHold**</span><span class="sxs-lookup"><span data-stu-id="3f1a7-133">**IADsHold**</span></span>](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





