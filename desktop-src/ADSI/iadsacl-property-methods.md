---
title: Métodos de la propiedad IADsAcl (iAds. h)
description: El método Property de la interfaz IADsAcl establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsAcl ADSI
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d8afb1ba3cbf7749ad8e3d14fa970662715909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492017"
---
# <a name="iadsacl-property-methods"></a><span data-ttu-id="d728a-105">Métodos de propiedad IADsAcl</span><span class="sxs-lookup"><span data-stu-id="d728a-105">IADsAcl Property Methods</span></span>

<span data-ttu-id="d728a-106">El método Property de la interfaz [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d728a-106">The property method of the [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) interface sets the property described in the following table.</span></span> <span data-ttu-id="d728a-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d728a-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d728a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d728a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d728a-109">**Privilegios**</span><span class="sxs-lookup"><span data-stu-id="d728a-109">**Privileges**</span></span>
<span data-ttu-id="d728a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d728a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d728a-111">Configuración de privilegios.</span><span class="sxs-lookup"><span data-stu-id="d728a-111">Privilege settings.</span></span>

<dt>

<span data-ttu-id="d728a-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d728a-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d728a-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d728a-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d728a-114">**ProtectedAttrName**</span><span class="sxs-lookup"><span data-stu-id="d728a-114">**ProtectedAttrName**</span></span>
<span data-ttu-id="d728a-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d728a-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d728a-116">Nombre de un atributo protegido.</span><span class="sxs-lookup"><span data-stu-id="d728a-116">Name of a protected attribute.</span></span>

<dt>

<span data-ttu-id="d728a-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d728a-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d728a-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d728a-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d728a-119">**SubjectName**</span><span class="sxs-lookup"><span data-stu-id="d728a-119">**SubjectName**</span></span>
<span data-ttu-id="d728a-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d728a-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d728a-121">Nombre del asunto.</span><span class="sxs-lookup"><span data-stu-id="d728a-121">Name of the subject.</span></span>

<dt>

<span data-ttu-id="d728a-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d728a-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d728a-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d728a-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="d728a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d728a-124">Requirements</span></span>



| <span data-ttu-id="d728a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d728a-125">Requirement</span></span> | <span data-ttu-id="d728a-126">Value</span><span class="sxs-lookup"><span data-stu-id="d728a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d728a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d728a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d728a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d728a-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d728a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d728a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d728a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d728a-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d728a-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d728a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d728a-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="d728a-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d728a-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d728a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d728a-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d728a-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d728a-135">IID</span><span class="sxs-lookup"><span data-stu-id="d728a-135">IID</span></span><br/>                      | <span data-ttu-id="d728a-136">IID \_ IADsAcl se define como 8452D3AB-0869-11D1-A377-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="d728a-136">IID\_IADsAcl is defined as 8452D3AB-0869-11D1-A377-00C04FB950DC</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="d728a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d728a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d728a-138">**IADsAcl**</span><span class="sxs-lookup"><span data-stu-id="d728a-138">**IADsAcl**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





