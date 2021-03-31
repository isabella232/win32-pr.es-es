---
title: Métodos de la propiedad IADsLocality (iAds. h)
description: Los métodos de la interfaz IADsLocality leen y escriben las propiedades descritas en este tema. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 5d1cea40-62fb-49d4-857f-4563e9db7f51
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsLocality ADSI
topic_type:
- apiref
api_name:
- IADsLocality Property Methods
- IADsLocality.Description
- IADsLocality.get_Description
- IADsLocality.put_Description
- IADsLocality.LocalityName
- IADsLocality.get_LocalityName
- IADsLocality.put_LocalityName
- IADsLocality.PostalAddress
- IADsLocality.get_PostalAddress
- IADsLocality.put_PostalAddress
- IADsLocality.SeeAlso
- IADsLocality.get_SeeAlso
- IADsLocality.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34023f0af5365deb4f023d53a843dcf688c40afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996833"
---
# <a name="iadslocality-property-methods"></a><span data-ttu-id="04185-105">Métodos de propiedad IADsLocality</span><span class="sxs-lookup"><span data-stu-id="04185-105">IADsLocality Property Methods</span></span>

<span data-ttu-id="04185-106">Los métodos de la interfaz [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) leen y escriben las propiedades descritas en este tema.</span><span class="sxs-lookup"><span data-stu-id="04185-106">The methods of the [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="04185-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="04185-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="04185-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04185-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="04185-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04185-109">**Description**</span></span>
<span data-ttu-id="04185-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="04185-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="04185-111">Indica el texto que describe la localidad.</span><span class="sxs-lookup"><span data-stu-id="04185-111">Indicates the text that describes the locality.</span></span>

<dt>

<span data-ttu-id="04185-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="04185-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="04185-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="04185-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="04185-114">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="04185-114">**LocalityName**</span></span>
<span data-ttu-id="04185-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="04185-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="04185-116">Indica el nombre de la región geográfica tal como lo representa este objeto de localidad.</span><span class="sxs-lookup"><span data-stu-id="04185-116">Indicates the name of the geographical region as represented by this locality object.</span></span>

<dt>

<span data-ttu-id="04185-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="04185-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="04185-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="04185-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="04185-119">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="04185-119">**PostalAddress**</span></span>
<span data-ttu-id="04185-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="04185-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="04185-121">Indica la dirección postal principal de la localidad.</span><span class="sxs-lookup"><span data-stu-id="04185-121">Indicates the main postal address of the locality.</span></span>

<dt>

<span data-ttu-id="04185-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="04185-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="04185-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="04185-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="04185-124">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="04185-124">**SeeAlso**</span></span>
<span data-ttu-id="04185-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="04185-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="04185-126">Indica una matriz de nombres ADsPath de objetos de directorio relevantes para este objeto.</span><span class="sxs-lookup"><span data-stu-id="04185-126">Indicates an array of ADsPath names of directory objects relevant to this object.</span></span>

<dt>

<span data-ttu-id="04185-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="04185-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="04185-128">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="04185-128">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="04185-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="04185-129">Examples</span></span>

<span data-ttu-id="04185-130">En el ejemplo de código siguiente se muestran los datos de ubicación de un objeto contenedor.</span><span class="sxs-lookup"><span data-stu-id="04185-130">The following code example displays the locality data of a container object.</span></span> <span data-ttu-id="04185-131">Se supone que se ha creado un objeto de localidad, denominado "locality", para el objeto contenedor y se han establecido las propiedades.</span><span class="sxs-lookup"><span data-stu-id="04185-131">It assumes that a locality object, named "myLocality", has been created for the container object and the properties have been set.</span></span>


```VB
Dim dom As IADsContainer
Dim loc As IADsLocality
On Error GoTo Cleanup
 
Set dom = getObject("LDAP://adsrv1/dc=Fabrikam, dc=Com")
Set loc = dom.GetObject("locality","L=myLocality")
Debug.Print loc.Name
Debug.Print loc.LocalityName
Debug.Print loc.Description
Debug.Print loc.PostalAddress
Debug.Print loc.SeeAlso

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dom = Nothing
    Set loc = Nothing
```



## <a name="requirements"></a><span data-ttu-id="04185-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04185-132">Requirements</span></span>



| <span data-ttu-id="04185-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="04185-133">Requirement</span></span> | <span data-ttu-id="04185-134">Value</span><span class="sxs-lookup"><span data-stu-id="04185-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04185-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04185-135">Minimum supported client</span></span><br/> | <span data-ttu-id="04185-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04185-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04185-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04185-137">Minimum supported server</span></span><br/> | <span data-ttu-id="04185-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04185-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04185-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04185-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="04185-140"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="04185-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="04185-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04185-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04185-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04185-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="04185-143">IID</span><span class="sxs-lookup"><span data-stu-id="04185-143">IID</span></span><br/>                      | <span data-ttu-id="04185-144">IID \_ IADsLocality se define como A05E03A2-Effe-11cf-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="04185-144">IID\_IADsLocality is defined as A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="04185-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="04185-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04185-146">**IADs**</span><span class="sxs-lookup"><span data-stu-id="04185-146">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="04185-147">**IADsLocality**</span><span class="sxs-lookup"><span data-stu-id="04185-147">**IADsLocality**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslocality)
</dt> <dt>

[<span data-ttu-id="04185-148">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="04185-148">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





