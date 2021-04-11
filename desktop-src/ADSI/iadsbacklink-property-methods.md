---
title: Métodos de la propiedad IADsBackLink (iAds. h)
description: El método Property de la interfaz IADsBackLink establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsBackLink ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150778"
---
# <a name="iadsbacklink-property-methods"></a><span data-ttu-id="49fc5-105">Métodos de propiedad IADsBackLink</span><span class="sxs-lookup"><span data-stu-id="49fc5-105">IADsBackLink Property Methods</span></span>

<span data-ttu-id="49fc5-106">El método Property de la interfaz [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="49fc5-106">The property method of the [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) interface sets the property described in the following table.</span></span> <span data-ttu-id="49fc5-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="49fc5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="49fc5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49fc5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="49fc5-109">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="49fc5-109">**ObjectName**</span></span>
<span data-ttu-id="49fc5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="49fc5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="49fc5-111">Nombre de un objeto al que está asociado el atributo de **vínculo hacia atrás** .</span><span class="sxs-lookup"><span data-stu-id="49fc5-111">The name of an object the **Back Link** attribute is attached to.</span></span>

<dt>

<span data-ttu-id="49fc5-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49fc5-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="49fc5-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="49fc5-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="49fc5-114">**RemoteID**</span><span class="sxs-lookup"><span data-stu-id="49fc5-114">**RemoteID**</span></span>
<span data-ttu-id="49fc5-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="49fc5-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="49fc5-116">Identificador del servidor remoto que requiere una referencia externa del objeto especificado por **objectname**.</span><span class="sxs-lookup"><span data-stu-id="49fc5-116">The identifier of the remote server that requires an external reference of the object specified by **ObjectName**.</span></span>

<dt>

<span data-ttu-id="49fc5-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49fc5-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="49fc5-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="49fc5-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="49fc5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49fc5-119">Requirements</span></span>



| <span data-ttu-id="49fc5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="49fc5-120">Requirement</span></span> | <span data-ttu-id="49fc5-121">Value</span><span class="sxs-lookup"><span data-stu-id="49fc5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49fc5-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49fc5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49fc5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49fc5-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49fc5-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49fc5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49fc5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49fc5-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49fc5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49fc5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="49fc5-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="49fc5-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="49fc5-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49fc5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49fc5-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49fc5-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="49fc5-130">IID</span><span class="sxs-lookup"><span data-stu-id="49fc5-130">IID</span></span><br/>                      | <span data-ttu-id="49fc5-131">IID \_ IADsBackLink se define como FD1302BD-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="49fc5-131">IID\_IADsBackLink is defined as FD1302BD-4080-11D1-A3AC-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="49fc5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="49fc5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fc5-133">**IADsBackLink**</span><span class="sxs-lookup"><span data-stu-id="49fc5-133">**IADsBackLink**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[<span data-ttu-id="49fc5-134">**\_BACKLINK ADS**</span><span class="sxs-lookup"><span data-stu-id="49fc5-134">**ADS\_BACKLINK**</span></span>](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 





