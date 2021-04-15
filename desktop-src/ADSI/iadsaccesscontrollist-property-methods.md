---
title: Métodos de la propiedad IADsAccessControlList (iAds. h)
description: Los métodos de propiedad de la interfaz IADsAccessControlList obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: cb68bb61-4216-4f69-bea1-ab7f98937a27
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsAccessControlList ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlList Property Methods
- IADsAccessControlList.AclRevision
- IADsAccessControlList.get_AclRevision
- IADsAccessControlList.put_AclRevision
- IADsAccessControlList.AceCount
- IADsAccessControlList.get_AceCount
- IADsAccessControlList.put_AceCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55763b7c52071ca5bfd0a875912941090b7992c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422051"
---
# <a name="iadsaccesscontrollist-property-methods"></a><span data-ttu-id="3d4c5-105">Métodos de propiedad IADsAccessControlList</span><span class="sxs-lookup"><span data-stu-id="3d4c5-105">IADsAccessControlList Property Methods</span></span>

<span data-ttu-id="3d4c5-106">Los métodos de propiedad de la interfaz [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-106">The property methods of the [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="3d4c5-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3d4c5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3d4c5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d4c5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3d4c5-109">**AceCount**</span><span class="sxs-lookup"><span data-stu-id="3d4c5-109">**AceCount**</span></span>
<span data-ttu-id="3d4c5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3d4c5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3d4c5-111">El número de entradas de control de acceso en la lista de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-111">The number of access control entries in the access-control list.</span></span>

<dt>

<span data-ttu-id="3d4c5-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3d4c5-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3d4c5-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="3d4c5-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceCount(
  [out] LONG* lnAceCount
);
HRESULT put_AceCount(
  [in] LONG lnAceCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3d4c5-114">**AclRevision**</span><span class="sxs-lookup"><span data-stu-id="3d4c5-114">**AclRevision**</span></span>
<span data-ttu-id="3d4c5-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3d4c5-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="3d4c5-116">El nivel de revisión de una lista de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-116">The revision level of an access-control list.</span></span> <span data-ttu-id="3d4c5-117">Este valor puede ser **la \_ revisión de ACL** o el DS de la **\_ revisión \_ de ACL**.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-117">This value can be **ACL\_REVISION** or **ACL\_REVISION\_DS**.</span></span> <span data-ttu-id="3d4c5-118">Use **la \_ revisión \_ de ACL DS** si la ACL contiene una ACE específica del objeto.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-118">Use **ACL\_REVISION\_DS** if the ACL contains an object-specific ACE.</span></span> <span data-ttu-id="3d4c5-119">Todas las ACE de una ACL deben estar en el mismo nivel de revisión.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-119">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="3d4c5-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3d4c5-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3d4c5-121">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="3d4c5-121">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AclRevision(
  [out] LONG* lnAclRevision
);
HRESULT put_AclRevision(
  [in] LONG lnAclRevision
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="3d4c5-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3d4c5-122">Examples</span></span>

<span data-ttu-id="3d4c5-123">En el ejemplo de código siguiente se muestra el número de ACE en una ACL.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-123">The following code example displays the number of ACEs in an ACL.</span></span>


```VB
Dim x as IADs
Dim sd As IADsSecurityDescriptor
Dim Dacl As IADsAccessControlList

On Error GoTo Cleanup

Set x = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
Debug.Print Dacl.AceCount

Cleanup:
    If (Err.Number <> 0) Then
        MsgBox ("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
```



<span data-ttu-id="3d4c5-124">En el ejemplo de código siguiente se muestra el número de ACE en una ACL.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-124">The following code example displays the number of ACEs in an ACL.</span></span>


```C++
HRESULT ShowACEInACL(LPWSTR guestPath,LPWSTR user,LPWSTR passwd)
{
  IADs *pObj = NULL;
  IADsSecurityDescriptor *psd = NULL;
  HRESULT hr = S_OK;
  VARIANT var;

  VariantInit(&var);

  hr = ADsOpenObject(guestPath,user,passwd,ADS_SECURE_AUTHENTICATION,
                     IID_IADs,(void**)&pObj);
  if(FAILED(hr)) {
      printf("hr = %x\n",hr);
      return hr;
  }
  else {
      BSTR bstr = NULL;
      pObj->get_Class(&bstr);
      printf("Object class: %S\n",bstr);
      SysFreeString(bstr);
  }

  hr = pObj->Get(CComBSTR("ntSecurityDescriptor"), &var);
  pObj->Release();

  if(FAILED(hr)) {
      printf("Get ntSD: hr = %x\n",hr);
      return hr;
  }

  hr = V_DISPATCH(&var)->QueryInterface(IID_IADsSecurityDescriptor,
                                        (void**)&psd);

  if(FAILED(hr)) {
      printf("DISP: hr = %x\n",hr);
      VariantClear(&var);
      return hr;
  }

  IDispatch *pDisp = NULL;
  hr = psd->get_DiscretionaryAcl(&pDisp);
  VariantClear(&var);

  if(FAILED(hr)) {
      printf("get_DACL : hr = %x\n",hr);
      return hr;
  }

  IADsAccessControlList *pAcl = NULL;
  hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pAcl);
  pDisp->Release();

  if(FAILED(hr)) {
      printf("QI ACL: hr = %x\n",hr);
      return hr;
  }

  long count = 0;
  hr = pAcl->get_AceCount(&count);
  pAcl->Release();
  if(FAILED(hr)) {
      printf("Count: hr = %x\n",hr);
      return hr;
  }

  printf("AceCount = %d\n",count);

  return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="3d4c5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d4c5-125">Requirements</span></span>



| <span data-ttu-id="3d4c5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d4c5-126">Requirement</span></span> | <span data-ttu-id="3d4c5-127">Value</span><span class="sxs-lookup"><span data-stu-id="3d4c5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4c5-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d4c5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3d4c5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d4c5-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3d4c5-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d4c5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3d4c5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d4c5-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3d4c5-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d4c5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d4c5-133"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d4c5-133"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="3d4c5-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d4c5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d4c5-135"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d4c5-135"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="3d4c5-136">IID</span><span class="sxs-lookup"><span data-stu-id="3d4c5-136">IID</span></span><br/>                      | <span data-ttu-id="3d4c5-137">IID \_ IADsAccessControlList se define como B7EE91CC-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="3d4c5-137">IID\_IADsAccessControlList is defined as B7EE91CC-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d4c5-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d4c5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4c5-139">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="3d4c5-139">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="3d4c5-140">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="3d4c5-140">**IEnumVARIANT**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[<span data-ttu-id="3d4c5-141">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="3d4c5-141">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="3d4c5-142">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3d4c5-142">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

