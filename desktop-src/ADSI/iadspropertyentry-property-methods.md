---
title: Métodos de la propiedad IADsPropertyEntry (iAds. h)
description: Proporcione acceso a las siguientes propiedades.
ms.assetid: 73b0f6d4-55db-46cf-a781-e10bc4fcf2db
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPropertyEntry ADSI
topic_type:
- apiref
api_name:
- IADsPropertyEntry Property Methods
- IADsPropertyEntry.Name
- IADsPropertyEntry.get_Name
- IADsPropertyEntry.put_Name
- IADsPropertyEntry.ADsType
- IADsPropertyEntry.get_ADsType
- IADsPropertyEntry.put_ADsType
- IADsPropertyEntry.ControlCode
- IADsPropertyEntry.get_ControlCode
- IADsPropertyEntry.put_ControlCode
- IADsPropertyEntry.Values
- IADsPropertyEntry.get_Values
- IADsPropertyEntry.put_Values
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e82344b2b659395bb14c0500fde3214530e000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905604"
---
# <a name="iadspropertyentry-property-methods"></a><span data-ttu-id="3c155-104">Métodos de propiedad IADsPropertyEntry</span><span class="sxs-lookup"><span data-stu-id="3c155-104">IADsPropertyEntry Property Methods</span></span>

<span data-ttu-id="3c155-105">Los métodos de propiedad de la interfaz [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) proporcionan acceso a las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="3c155-105">The property methods of the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface provide access to the following properties.</span></span> <span data-ttu-id="3c155-106">Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3c155-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3c155-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c155-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3c155-108">**ADsType**</span><span class="sxs-lookup"><span data-stu-id="3c155-108">**ADsType**</span></span>
<span data-ttu-id="3c155-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3c155-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="3c155-110">El tipo de datos de la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="3c155-110">The data type of the **Name** property.</span></span> <span data-ttu-id="3c155-111">Los valores del tipo de datos se definen en la enumeración [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) .</span><span class="sxs-lookup"><span data-stu-id="3c155-111">The values of the data type is defined in the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration.</span></span>

<dt>

<span data-ttu-id="3c155-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3c155-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c155-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="3c155-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* plADsType
);
HRESULT put_ADsType(
  [in] LONG lADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3c155-114">**ControlCode**</span><span class="sxs-lookup"><span data-stu-id="3c155-114">**ControlCode**</span></span>
<span data-ttu-id="3c155-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3c155-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="3c155-116">Constante que especifica la operación que se va a realizar en la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="3c155-116">A constant that specifies the operation to be performed on the named property.</span></span> <span data-ttu-id="3c155-117">El valor se define en la enumeración de la enumeración de la [**\_ operación de propiedad \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="3c155-117">The value is defined in the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="3c155-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3c155-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c155-119">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="3c155-119">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ControlCode(
  [out] LONG* pControlCode
);
HRESULT put_ControlCode(
  [in] LONG lnControlCode
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3c155-120">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3c155-120">**Name**</span></span>
<span data-ttu-id="3c155-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3c155-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="3c155-122">Nombre de la entrada de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c155-122">Name of the property entry.</span></span> <span data-ttu-id="3c155-123">Este nombre debe corresponder al nombre de un atributo tal y como se define en el esquema.</span><span class="sxs-lookup"><span data-stu-id="3c155-123">This name should correspond to the name of an attribute as defined in the schema.</span></span>

<dt>

<span data-ttu-id="3c155-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3c155-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c155-125">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3c155-125">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
HRESULT put_Name(
  [in] BSTR bstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3c155-126">**Valores**</span><span class="sxs-lookup"><span data-stu-id="3c155-126">**Values**</span></span>
<span data-ttu-id="3c155-127"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3c155-127"></dt> <dd> <dl></span></span>

<span data-ttu-id="3c155-128">Matriz de **tipo Variant** .</span><span class="sxs-lookup"><span data-stu-id="3c155-128">A **VARIANT** array.</span></span> <span data-ttu-id="3c155-129">Cada elemento de esta matriz representa un valor de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="3c155-129">Each element in this array represents a value of the named property.</span></span> <span data-ttu-id="3c155-130">Estos valores de propiedad se representan mediante objetos ADSI que implementan las interfaces [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) y [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) .</span><span class="sxs-lookup"><span data-stu-id="3c155-130">Such property values are represented by ADSI objects implementing the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) and [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interfaces.</span></span> <span data-ttu-id="3c155-131">Por lo tanto, la matriz **Variant** contiene una matriz de punteros a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en los objetos ADSI que implementan las interfaces **IADsPropertyValue** y **IADsPropertyValue2** .</span><span class="sxs-lookup"><span data-stu-id="3c155-131">Therefore, the **VARIANT** array holds an array of pointers to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface on the ADSI objects implementing the **IADsPropertyValue** and **IADsPropertyValue2** interfaces.</span></span>

<dt>

<span data-ttu-id="3c155-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3c155-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c155-133">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="3c155-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Values(
  [out] VARIANT* pvValues
);
HRESULT put_Values(
  [in] VARIANT vValues
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="3c155-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c155-134">Remarks</span></span>

<span data-ttu-id="3c155-135">Cada método de propiedad admite los valores devueltos de **HRESULT** estándar, incluidos los que son \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="3c155-135">Each property method supports the standard **HRESULT** return values, including S\_OK.</span></span> <span data-ttu-id="3c155-136">Para obtener más información sobre otros valores devueltos, consulte [códigos de error ADSI](adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3c155-136">For more information about other return values, see [ADSI Error Codes](adsi-error-codes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3c155-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3c155-137">Examples</span></span>

<span data-ttu-id="3c155-138">En el ejemplo de código siguiente se muestra cómo recuperar una propiedad con nombre de la memoria caché y crear una nueva entrada de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c155-138">The following code example shows how to retrieve a named property from the cache and create a new property entry.</span></span>


```VB
 
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup

'------------------------------------------------------------
'----- Getting IADsPropertyEntry ----------------------------
'------------------------------------------------------------
 
' Create the property list object.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a named property entry object.
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)

' Insert code to do something with propEntry
Set propEntry = Nothing
 
'------------------------------------------------------------
'---- Setting IADsPropertyEntry -----------------------------
'------------------------------------------------------------
 
' Create a property value object.
Set propVal = New PropertyValue
 
'---- Property Value -----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'---- Create a new Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' ---- Put the newly created property entry to the cache ----
propList.PutPropertyItem (propEntry)
 
' Commit the entry to the directory store.
propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="3c155-139">En el ejemplo de código siguiente se muestra cómo obtener una propiedad con nombre de una memoria caché.</span><span class="sxs-lookup"><span data-stu-id="3c155-139">The following code example shows how to get a named property from a cache.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADs *pObj = NULL;
VARIANT var;
long valType = ADSTYPE_CASE_IGNORE_STRING;
 
VariantInit(&var);
 
// Bind to directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){return;}
 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), valType, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Get the name and the type of the property entry.
BSTR nm = NULL;
hr = pEntry->get_Name(&nm);
printf("Property name = %S\n",nm);
VariantClear(&var);
long at;
hr = pEntry->get_ADsType(&at);
printf("Property type = %d\n",a);

Cleanup:
    if(nm)
        SysFreeString(nm);

    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pObj)
        pObj->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="3c155-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c155-140">Requirements</span></span>



| <span data-ttu-id="3c155-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c155-141">Requirement</span></span> | <span data-ttu-id="3c155-142">Value</span><span class="sxs-lookup"><span data-stu-id="3c155-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c155-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c155-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3c155-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c155-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c155-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c155-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3c155-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c155-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c155-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c155-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c155-148"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c155-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3c155-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c155-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c155-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c155-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3c155-151">IID</span><span class="sxs-lookup"><span data-stu-id="3c155-151">IID</span></span><br/>                      | <span data-ttu-id="3c155-152">IID \_ IADsPropertyEntry se define como 05792C8E-941F-11D0-8529-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="3c155-152">IID\_IADsPropertyEntry is defined as 05792C8E-941F-11D0-8529-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="3c155-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c155-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c155-154">**\_ \_ enumeración de operación de propiedad ADS \_**</span><span class="sxs-lookup"><span data-stu-id="3c155-154">**ADS\_PROPERTY\_OPERATION\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)
</dt> <dt>

[<span data-ttu-id="3c155-155">Códigos de error ADSI</span><span class="sxs-lookup"><span data-stu-id="3c155-155">ADSI Error Codes</span></span>](adsi-error-codes.md)
</dt> <dt>

[<span data-ttu-id="3c155-156">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="3c155-156">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="3c155-157">**IADsPropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="3c155-157">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="3c155-158">**IADsPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="3c155-158">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="3c155-159">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="3c155-159">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="3c155-160">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="3c155-160">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

