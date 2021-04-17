---
title: Métodos de la propiedad IADsOU (iAds. h)
description: Los métodos de propiedad de la interfaz IADsOU obtienen o establecen las propiedades enumeradas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsOU ADSI
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ce30fad6a690a26a8e16b817b77b129dee25f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658298"
---
# <a name="iadsou-property-methods"></a><span data-ttu-id="b00a8-105">Métodos de propiedad IADsOU</span><span class="sxs-lookup"><span data-stu-id="b00a8-105">IADsOU Property Methods</span></span>

<span data-ttu-id="b00a8-106">Los métodos de propiedad de la interfaz [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) obtienen o establecen las propiedades enumeradas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b00a8-106">The property methods of the [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="b00a8-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b00a8-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b00a8-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b00a8-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b00a8-109">**BusinessCategory**</span><span class="sxs-lookup"><span data-stu-id="b00a8-109">**BusinessCategory**</span></span>
<span data-ttu-id="b00a8-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b00a8-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="b00a8-111">Una cadena que contiene las funciones empresariales generales que realiza la unidad organizativa, por ejemplo "contabilidad".</span><span class="sxs-lookup"><span data-stu-id="b00a8-111">A string that contains the general business function or functions performed by the organizational unit, for example "Accounting".</span></span>

<dt>

<span data-ttu-id="b00a8-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b00a8-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b00a8-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b00a8-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b00a8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b00a8-114">**Description**</span></span>
<span data-ttu-id="b00a8-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b00a8-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="b00a8-116">Cadena que contiene una descripción textual de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="b00a8-116">A string that contains a textual description of the organizational unit.</span></span>

<dt>

<span data-ttu-id="b00a8-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b00a8-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b00a8-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b00a8-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="b00a8-119">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="b00a8-119">**FaxNumber**</span></span>
<span data-ttu-id="b00a8-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b00a8-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="b00a8-121">Una cadena que contiene el número de facsímil de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="b00a8-121">A string that contains the facsimile number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="b00a8-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b00a8-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b00a8-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b00a8-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="b00a8-124">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="b00a8-124">**LocalityName**</span></span>
<span data-ttu-id="b00a8-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b00a8-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="b00a8-126">Una cadena que contiene el nombre de la región geográfica de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="b00a8-126">A string that contains the name of the geographic region of the organizational unit.</span></span>

<dt>

<span data-ttu-id="b00a8-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b00a8-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b00a8-128">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b00a8-128">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="b00a8-129">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="b00a8-129">**PostalAddress**</span></span>
<span data-ttu-id="b00a8-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b00a8-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="b00a8-131">Cadena que contiene la dirección postal de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="b00a8-131">A string that contains the postal address of the organizational unit.</span></span>

<dt>

<span data-ttu-id="b00a8-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b00a8-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b00a8-133">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b00a8-133">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="b00a8-134">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="b00a8-134">**SeeAlso**</span></span>
<span data-ttu-id="b00a8-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b00a8-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="b00a8-136">Matriz de cadenas que contiene los nombres distintivos de otros objetos de directorio que pueden ser pertinentes para este objeto.</span><span class="sxs-lookup"><span data-stu-id="b00a8-136">An array of strings that contains the distinguished names of other directory objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="b00a8-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b00a8-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b00a8-138">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="b00a8-138">Scripting data type: **VARIANT**</span></span>
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

<span data-ttu-id="b00a8-139">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="b00a8-139">**TelephoneNumber**</span></span>
<span data-ttu-id="b00a8-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b00a8-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="b00a8-141">Cadena que contiene el número de teléfono de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="b00a8-141">A string that contains the telephone number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="b00a8-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b00a8-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b00a8-143">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b00a8-143">Scripting data type: **BSTR**</span></span>
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

 

## <a name="examples"></a><span data-ttu-id="b00a8-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b00a8-144">Examples</span></span>

<span data-ttu-id="b00a8-145">En el ejemplo de código siguiente se muestra el **BusinessCategory** y la **Descripción** de todas las unidades de organización en un contenedor.</span><span class="sxs-lookup"><span data-stu-id="b00a8-145">The following code example displays the **BusinessCategory** and **Description** of all organization units in a container.</span></span> <span data-ttu-id="b00a8-146">Se supone que el servicio de directorio subyacente admite la agrupación de objetos de directorio por unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="b00a8-146">It assumes that the underlying directory service supports grouping of directory objects by organization unit.</span></span>


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a><span data-ttu-id="b00a8-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b00a8-147">Requirements</span></span>



| <span data-ttu-id="b00a8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="b00a8-148">Requirement</span></span> | <span data-ttu-id="b00a8-149">Value</span><span class="sxs-lookup"><span data-stu-id="b00a8-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b00a8-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b00a8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b00a8-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b00a8-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b00a8-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b00a8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b00a8-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b00a8-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b00a8-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b00a8-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="b00a8-155"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="b00a8-155"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b00a8-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b00a8-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b00a8-157"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b00a8-157"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b00a8-158">IID</span><span class="sxs-lookup"><span data-stu-id="b00a8-158">IID</span></span><br/>                      | <span data-ttu-id="b00a8-159">IID \_ IADsOU se define como A2F733B8-Effe-11cf-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="b00a8-159">IID\_IADsOU is defined as A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b00a8-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="b00a8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b00a8-161">**IADsOU**</span><span class="sxs-lookup"><span data-stu-id="b00a8-161">**IADsOU**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[<span data-ttu-id="b00a8-162">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="b00a8-162">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





