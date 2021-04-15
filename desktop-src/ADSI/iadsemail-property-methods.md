---
title: Métodos de la propiedad IADsEmail (iAds. h)
description: El método Property de la interfaz IADsEmail establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsEmail ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422518"
---
# <a name="iadsemail-property-methods"></a><span data-ttu-id="c2e53-105">Métodos de propiedad IADsEmail</span><span class="sxs-lookup"><span data-stu-id="c2e53-105">IADsEmail Property Methods</span></span>

<span data-ttu-id="c2e53-106">El método Property de la interfaz [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c2e53-106">The property method of the [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) interface sets the property described in the following table.</span></span> <span data-ttu-id="c2e53-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c2e53-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c2e53-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2e53-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c2e53-109">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="c2e53-109">**Address**</span></span>
<span data-ttu-id="c2e53-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c2e53-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c2e53-111">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="c2e53-111">The email address of the user.</span></span>

<dt>

<span data-ttu-id="c2e53-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2e53-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c2e53-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c2e53-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2e53-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c2e53-114">**Type**</span></span>
<span data-ttu-id="c2e53-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c2e53-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="c2e53-116">El tipo del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c2e53-116">The type of the email message.</span></span>

<dt>

<span data-ttu-id="c2e53-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2e53-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c2e53-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="c2e53-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="c2e53-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e53-119">Requirements</span></span>



| <span data-ttu-id="c2e53-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e53-120">Requirement</span></span> | <span data-ttu-id="c2e53-121">Value</span><span class="sxs-lookup"><span data-stu-id="c2e53-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e53-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2e53-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e53-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2e53-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2e53-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2e53-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e53-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2e53-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2e53-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2e53-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e53-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e53-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c2e53-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2e53-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2e53-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2e53-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c2e53-130">IID</span><span class="sxs-lookup"><span data-stu-id="c2e53-130">IID</span></span><br/>                      | <span data-ttu-id="c2e53-131">IID \_ IADsEmail se define como 97AF011A-478E-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="c2e53-131">IID\_IADsEmail is defined as 97AF011A-478E-11D1-A3B4-00C04FB950DC</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c2e53-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2e53-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e53-133">**IADsEmail**</span><span class="sxs-lookup"><span data-stu-id="c2e53-133">**IADsEmail**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[<span data-ttu-id="c2e53-134">**\_correo electrónico de ADS**</span><span class="sxs-lookup"><span data-stu-id="c2e53-134">**ADS\_EMAIL**</span></span>](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 





