---
title: Métodos de la propiedad IADsO (iAds. h)
description: Los métodos de propiedad de la interfaz IADsO obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: d4bc1d29-98de-462d-b59c-2bc2641c25a0
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsO ADSI
topic_type:
- apiref
api_name:
- IADsO Property Methods
- IADsO.Description
- IADsO.get_Description
- IADsO.put_Description
- IADsO.FaxNumber
- IADsO.get_FaxNumber
- IADsO.put_FaxNumber
- IADsO.LocalityName
- IADsO.get_LocalityName
- IADsO.put_LocalityName
- IADsO.PostalAddress
- IADsO.get_PostalAddress
- IADsO.put_PostalAddress
- IADsO.TelephoneNumber
- IADsO.get_TelephoneNumber
- IADsO.put_TelephoneNumber
- IADsO.SeeAlso
- IADsO.get_SeeAlso
- IADsO.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09840cf62d6883eb4f5ca326998b697a34698c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803164"
---
# <a name="iadso-property-methods"></a><span data-ttu-id="b9c5c-105">Métodos de propiedad IADsO</span><span class="sxs-lookup"><span data-stu-id="b9c5c-105">IADsO Property Methods</span></span>

<span data-ttu-id="b9c5c-106">Los métodos de propiedad de la interfaz [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-106">The property methods of the [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="b9c5c-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b9c5c-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b9c5c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9c5c-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b9c5c-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-109">**Description**</span></span>
<span data-ttu-id="b9c5c-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b9c5c-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="b9c5c-111">La descripción de la organización.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-111">The description of the organization.</span></span>

<dt>

<span data-ttu-id="b9c5c-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9c5c-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9c5c-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="b9c5c-114">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-114">**FaxNumber**</span></span>
<span data-ttu-id="b9c5c-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b9c5c-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="b9c5c-116">El número de facsímil (fax) de la organización.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-116">The facsimile (fax) number of the organization.</span></span>

<dt>

<span data-ttu-id="b9c5c-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9c5c-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9c5c-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9c5c-119">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-119">**LocalityName**</span></span>
<span data-ttu-id="b9c5c-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b9c5c-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="b9c5c-121">Nombre del lugar en el que se encuentra la organización.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-121">The name of the place in which the organization is located.</span></span>

<dt>

<span data-ttu-id="b9c5c-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9c5c-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9c5c-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="b9c5c-124">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-124">**PostalAddress**</span></span>
<span data-ttu-id="b9c5c-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b9c5c-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="b9c5c-126">Dirección postal de la organización.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-126">The postal address of the organization.</span></span>

<dt>

<span data-ttu-id="b9c5c-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9c5c-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9c5c-128">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-128">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="b9c5c-129">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-129">**SeeAlso**</span></span>
<span data-ttu-id="b9c5c-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b9c5c-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="b9c5c-131">Una matriz de nombres ADsPath de otros objetos ADSI que puede ser relevante para este objeto.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-131">An array of ADsPath names of other ADSI objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="b9c5c-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9c5c-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9c5c-133">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-133">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9c5c-134">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-134">**TelephoneNumber**</span></span>
<span data-ttu-id="b9c5c-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b9c5c-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="b9c5c-136">Número de teléfono de la organización.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-136">The telephone number of the organization.</span></span>

<dt>

<span data-ttu-id="b9c5c-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9c5c-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9c5c-138">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="b9c5c-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b9c5c-139">Examples</span></span>

<span data-ttu-id="b9c5c-140">En el ejemplo de código siguiente se muestra la descripción de una organización determinada.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-140">The following code example displays the description of a given organization.</span></span> <span data-ttu-id="b9c5c-141">Se supone que el servicio de directorio subyacente admite la agrupación de objetos de directorio por organización.</span><span class="sxs-lookup"><span data-stu-id="b9c5c-141">It assumes the underlying directory service supports grouping directory objects by organization.</span></span>


```VB
Dim dom As IADsContainer
Dim dso As IADsOpenDSObject
Dim szUsername As String
Dim szPassword As String
On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password
 
Set dso = GetObject("LDAP:")
Set dom = dso.OpenDSObject("LDAP://adsrv1/dc=Fabrikam, dc=Com", _
                           szUsername, szPassword,1)
dom.Filter = Array("organization")
For Each o In dom
    MsgBox "Fax number of " & o.Name & " : " & o.Description
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set dom = Nothing
    Set dso = Nothing
```



## <a name="requirements"></a><span data-ttu-id="b9c5c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9c5c-142">Requirements</span></span>



| <span data-ttu-id="b9c5c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9c5c-143">Requirement</span></span> | <span data-ttu-id="b9c5c-144">Value</span><span class="sxs-lookup"><span data-stu-id="b9c5c-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c5c-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9c5c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c5c-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9c5c-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9c5c-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9c5c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c5c-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9c5c-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9c5c-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9c5c-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9c5c-150"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9c5c-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b9c5c-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9c5c-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9c5c-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9c5c-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b9c5c-153">IID</span><span class="sxs-lookup"><span data-stu-id="b9c5c-153">IID</span></span><br/>                      | <span data-ttu-id="b9c5c-154">IID \_ IADsO se define como A1CD2DC6-Effe-11cf-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="b9c5c-154">IID\_IADsO is defined as A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b9c5c-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9c5c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c5c-156">**IADsO**</span><span class="sxs-lookup"><span data-stu-id="b9c5c-156">**IADsO**</span></span>](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[<span data-ttu-id="b9c5c-157">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="b9c5c-157">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





