---
title: Métodos de la propiedad IADsAccessControlEntry (iAds. h)
description: Los métodos de propiedad de la interfaz IADsAccessControlEntry obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: dce11723-0e30-4baa-8666-0a32f0968ebb
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsAccessControlEntry ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlEntry Property Methods
- IADsAccessControlEntry.AccessMask
- IADsAccessControlEntry.get_AccessMask
- IADsAccessControlEntry.put_AccessMask
- IADsAccessControlEntry.AceType
- IADsAccessControlEntry.get_AceType
- IADsAccessControlEntry.put_AceType
- IADsAccessControlEntry.AceFlags
- IADsAccessControlEntry.get_AceFlags
- IADsAccessControlEntry.put_AceFlags
- IADsAccessControlEntry.Flags
- IADsAccessControlEntry.get_Flags
- IADsAccessControlEntry.put_Flags
- IADsAccessControlEntry.ObjectType
- IADsAccessControlEntry.get_ObjectType
- IADsAccessControlEntry.put_ObjectType
- IADsAccessControlEntry.InheritedObjectType
- IADsAccessControlEntry.get_InheritedObjectType
- IADsAccessControlEntry.put_InheritedObjectType
- IADsAccessControlEntry.Trustee
- IADsAccessControlEntry.get_Trustee
- IADsAccessControlEntry.put_Trustee
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8539807f21944ab6f4b2c03f04b14a53dffdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801544"
---
# <a name="iadsaccesscontrolentry-property-methods"></a><span data-ttu-id="75bcf-105">Métodos de propiedad IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="75bcf-105">IADsAccessControlEntry Property Methods</span></span>

<span data-ttu-id="75bcf-106">Los métodos de propiedad de la interfaz [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="75bcf-106">The property methods of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="75bcf-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="75bcf-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="75bcf-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75bcf-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="75bcf-109">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="75bcf-109">**AccessMask**</span></span>
<span data-ttu-id="75bcf-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75bcf-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="75bcf-111">Contiene un conjunto de marcas que especifican los privilegios de acceso para el objeto.</span><span class="sxs-lookup"><span data-stu-id="75bcf-111">Contains a set of flags that specifies access privileges for the object.</span></span> <span data-ttu-id="75bcf-112">Los valores válidos para los objetos Active Directory se definen en la enumeración [**ADS \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum) .</span><span class="sxs-lookup"><span data-stu-id="75bcf-112">Valid values for Active Directory objects are defined in the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration.</span></span>

<span data-ttu-id="75bcf-113">Para obtener más información y una lista de los posibles valores para los objetos de recurso compartido de archivos o archivos, vea [seguridad de archivos y derechos de acceso](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="75bcf-113">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="75bcf-114">Para obtener más información y una lista de los posibles valores de los objetos del registro, consulte [seguridad y derechos de acceso de la clave del registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="75bcf-114">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

<dt>

<span data-ttu-id="75bcf-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75bcf-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75bcf-116">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="75bcf-116">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccessMask(
  [out] LONG* plnAccessMask
);
HRESULT put_AccessMask(
  [in] LONG lnAccessMask
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="75bcf-117">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="75bcf-117">**AceFlags**</span></span>
<span data-ttu-id="75bcf-118"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75bcf-118"></dt> <dd> <dl></span></span>

<span data-ttu-id="75bcf-119">Contiene un conjunto de marcas que especifica si otros contenedores u objetos pueden heredar la ACE.</span><span class="sxs-lookup"><span data-stu-id="75bcf-119">Contains a set of flags that specifies if other containers or objects can inherit the ACE.</span></span> <span data-ttu-id="75bcf-120">Los valores válidos para Active Directory objeto se definen en la enumeración de enumeración [**ADS \_ ACEFLAG \_**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) .</span><span class="sxs-lookup"><span data-stu-id="75bcf-120">Valid values for Active Directory object are defined in the [**ADS\_ACEFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) enumeration.</span></span>

<span data-ttu-id="75bcf-121">Para obtener más información y los posibles valores de los objetos de archivo, recurso compartido de archivos y registro, vea el miembro **AceFlags** de la estructura de [**\_ encabezado ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="75bcf-121">For more information and possible values for file, file share, and registry objects, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="75bcf-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75bcf-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75bcf-123">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="75bcf-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceFlags(
  [out] LONG* plnAceFlags
);
HRESULT put_AceFlags(
  [in] LONG lnAceFlags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="75bcf-124">**AceType**</span><span class="sxs-lookup"><span data-stu-id="75bcf-124">**AceType**</span></span>
<span data-ttu-id="75bcf-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75bcf-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="75bcf-126">Contiene un valor que indica el tipo de ACE.</span><span class="sxs-lookup"><span data-stu-id="75bcf-126">Contains a value that indicates the type of ACE.</span></span> <span data-ttu-id="75bcf-127">Los valores válidos para los objetos Active Directory se definen en la enumeración de enumeración [**ADS \_ ACETYPE \_**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) .</span><span class="sxs-lookup"><span data-stu-id="75bcf-127">Valid values for Active Directory objects are defined in the [**ADS\_ACETYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) enumeration.</span></span>

<span data-ttu-id="75bcf-128">Para obtener más información y los posibles valores de los objetos de archivo, recurso compartido de archivos y registro, vea el miembro **AceType** de la estructura de [**\_ encabezado ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="75bcf-128">For more information and possible values for file, file share, and registry objects, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="75bcf-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75bcf-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75bcf-130">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="75bcf-130">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceType(
  [out] LONG* plAceType
);
HRESULT put_AceType(
  [in] LONG lnAceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="75bcf-131">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="75bcf-131">**Flags**</span></span>
<span data-ttu-id="75bcf-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75bcf-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="75bcf-133">Marca que indica si la ACE tiene un tipo de objeto o un tipo de objeto heredado.</span><span class="sxs-lookup"><span data-stu-id="75bcf-133">A flag that indicates if the ACE has an object type or inherited object type.</span></span> <span data-ttu-id="75bcf-134">Las marcas válidas se definen en la enumeración de [**\_ \_ enumeración ADS FLAGTYPE**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) .</span><span class="sxs-lookup"><span data-stu-id="75bcf-134">Valid flags are defined in the [**ADS\_FLAGTYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="75bcf-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75bcf-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75bcf-136">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="75bcf-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Flags(
  [out] LONG* lnflags
);
HRESULT put_Flags(
  [in] LONG lnflags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="75bcf-137">**InheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="75bcf-137">**InheritedObjectType**</span></span>
<span data-ttu-id="75bcf-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75bcf-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="75bcf-139">Marca que indica el tipo de un objeto secundario de un objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="75bcf-139">A flag that indicates the type of a child object of an ADSI object.</span></span> <span data-ttu-id="75bcf-140">Su valor es un **GUID** de un objeto en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="75bcf-140">Its value is a **GUID** to an object in string format.</span></span> <span data-ttu-id="75bcf-141">Cuando se establece un **GUID** de este tipo, la ACE solo se aplica al objeto al que hace referencia el **GUID**.</span><span class="sxs-lookup"><span data-stu-id="75bcf-141">When such a **GUID** is set, the ACE applies only to the object referred to by the **GUID**.</span></span>

<dt>

<span data-ttu-id="75bcf-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75bcf-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75bcf-143">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="75bcf-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_InheritedObjectType(
  [out] BSTR* bstrInheritedObjectType
);
HRESULT put_InheritedObjectType(
  [in] BSTR bstrInheritedObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="75bcf-144">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="75bcf-144">**ObjectType**</span></span>
<span data-ttu-id="75bcf-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75bcf-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="75bcf-146">Marca que indica el tipo de objeto de ADSI.</span><span class="sxs-lookup"><span data-stu-id="75bcf-146">A flag that indicates the ADSI object type.</span></span> <span data-ttu-id="75bcf-147">Su valor es un **GUID** para una propiedad o un objeto en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="75bcf-147">Its value is a **GUID** to a property or an object in string format.</span></span> <span data-ttu-id="75bcf-148">El **GUID** hace referencia a una propiedad cuando se usan las máscaras de acceso ad **\_ right \_ DS \_ Read \_ prop** y **ADS \_ right \_ DS \_ Write \_ prop** .</span><span class="sxs-lookup"><span data-stu-id="75bcf-148">The **GUID** refers to a property when **ADS\_RIGHT\_DS\_READ\_PROP** and **ADS\_RIGHT\_DS\_WRITE\_PROP** access masks are used.</span></span> <span data-ttu-id="75bcf-149">El **GUID** especifica un objeto cuando se usan las máscaras de acceso de **\_ \_ DS \_ \_ Create** secundario de ad Right y **ADS \_ right \_ DS \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="75bcf-149">The **GUID** specifies an object when **ADS\_RIGHT\_DS\_CREATE\_CHILD** and **ADS\_RIGHT\_DS\_DELETE\_CHILD** access masks are used.</span></span>

<dt>

<span data-ttu-id="75bcf-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75bcf-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75bcf-151">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="75bcf-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectType(
  [out] BSTR* bstrObjectType
);
HRESULT put_ObjectType(
  [in] BSTR bstrObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="75bcf-152">**Confianza**</span><span class="sxs-lookup"><span data-stu-id="75bcf-152">**Trustee**</span></span>
<span data-ttu-id="75bcf-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75bcf-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="75bcf-154">Contiene el nombre de la cuenta a la que se aplica la ACE.</span><span class="sxs-lookup"><span data-stu-id="75bcf-154">Contains the name of the account that the ACE applies to.</span></span>

<dt>

<span data-ttu-id="75bcf-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75bcf-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75bcf-156">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="75bcf-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Trustee(
  [out] BSTR* pbstrSecurityId
);
HRESULT put_Trustee(
  [in] BSTR bstrSecurityId
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="75bcf-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="75bcf-157">Examples</span></span>

<span data-ttu-id="75bcf-158">En el ejemplo de código siguiente se muestra cómo agregar entradas a una ACL discrecional mediante los métodos de la propiedad [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="75bcf-158">The following code example shows how to add entries to a discretionary ACL using the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property methods.</span></span>


```VB
Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim ace As IADsAccessControlEntry
Dim Dacl As IADsAccessControlList
Dim Ace1 As New AccessControlEntry
Dim Ace2 As New AccessControlEntry

On Error GoTo Cleanup
 
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
 
' Show the existing ACEs.
For Each ace In Dacl
  Debug.Print ace.Trustee
Next
 
 
' Setup the first ACE.
Ace1.AccessMask = -1 'Full Permission (Allowed)
Ace1.AceType = ADS_ACETYPE_ACCESS_ALLOWED
Ace1.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace1.Trustee = "ACTIVED\Administrator"
 
' Setup the 2nd ACE.
Ace2.AccessMask = -1 'Full Permission (Denied)
Ace2.AceType = ADS_ACETYPE_ACCESS_DENIED
Ace2.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace2.Trustee = "ACTIVED\Andyhar"
 
' Add the ACEs to the Discretionary ACL.
Dacl.AddAce Ace1
Dacl.AddAce Ace2
 
sd.DiscretionaryAcl = Dacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set x = Nothing
    Set sd = Nothing
    Set ace = Nothing
    Set Dacl = Nothing
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set obj = Nothing
    Set cls = Nothing
```



<span data-ttu-id="75bcf-159">En el ejemplo de código siguiente se muestran las entradas de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="75bcf-159">The following code example displays access-control entries.</span></span>


```C++
IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs->Get(CComBSTR("ntSecurityDescriptor"),&var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&var);

hr = pDisp->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp->Release();


pSD->get_DiscretionaryAcl(&pDisp);

hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&var);

Cleanup:
    if(pADs) pADs->Release();
    if(pDisp) pDisp->Release();
    if(pSD) pSD->Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&var);
    
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum->Next(1,&var,&nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&var);
            hr = pDisp->QueryInterface(IID_IADsAccessControlEntry,(void**)&pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE->get_Trustee(&bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE->Release();
                pACE = NULL;
                pDisp->Release();
                pDisp = NULL;
            }       
            
            VariantClear(&var);
        }       
        hr = pEnum->Next(1,&var,&nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp->Release();
    if(pACL) pACL->Release();
    if(pACE) pACE->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="75bcf-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75bcf-160">Requirements</span></span>



| <span data-ttu-id="75bcf-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="75bcf-161">Requirement</span></span> | <span data-ttu-id="75bcf-162">Value</span><span class="sxs-lookup"><span data-stu-id="75bcf-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="75bcf-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75bcf-163">Minimum supported client</span></span><br/> | <span data-ttu-id="75bcf-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75bcf-164">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="75bcf-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75bcf-165">Minimum supported server</span></span><br/> | <span data-ttu-id="75bcf-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75bcf-166">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="75bcf-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75bcf-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="75bcf-168"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="75bcf-168"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="75bcf-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75bcf-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75bcf-170"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75bcf-170"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="75bcf-171">IID</span><span class="sxs-lookup"><span data-stu-id="75bcf-171">IID</span></span><br/>                      | <span data-ttu-id="75bcf-172">IID \_ IADsAccessControlEntry se define como B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="75bcf-172">IID\_IADsAccessControlEntry is defined as B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75bcf-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="75bcf-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75bcf-174">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="75bcf-174">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="75bcf-175">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="75bcf-175">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="75bcf-176">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="75bcf-176">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

