---
title: Métodos de la propiedad IADsGroup (iAds. h)
description: Métodos de propiedad de la interfaz IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsGroup ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658303"
---
# <a name="iadsgroup-property-methods"></a><span data-ttu-id="b632f-104">Métodos de propiedad IADsGroup</span><span class="sxs-lookup"><span data-stu-id="b632f-104">IADsGroup Property Methods</span></span>

<span data-ttu-id="b632f-105">Los métodos de propiedad de la interfaz [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) leen y escriben las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="b632f-105">The property methods of the [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) interface read and write the following properties.</span></span> <span data-ttu-id="b632f-106">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b632f-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b632f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b632f-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b632f-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b632f-108">**Description**</span></span>
<span data-ttu-id="b632f-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b632f-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="b632f-110">Indica la descripción textual de la pertenencia al grupo.</span><span class="sxs-lookup"><span data-stu-id="b632f-110">Indicates the textual description of the group membership.</span></span>

<dt>

<span data-ttu-id="b632f-111">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b632f-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b632f-112">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b632f-112">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="b632f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b632f-113">Remarks</span></span>

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a><span data-ttu-id="b632f-114">Usar IADsGroup para recuperar descripciones de grupos integrados</span><span class="sxs-lookup"><span data-stu-id="b632f-114">Using IADsGroup to Retrieve Descriptions of Built-in Groups</span></span>

<span data-ttu-id="b632f-115">En los siguientes ejemplos se muestra cómo recuperar información acerca de los objetos de grupo de Windows por nombre.</span><span class="sxs-lookup"><span data-stu-id="b632f-115">The following examples show how to retrieve information about Windows group objects by name.</span></span> <span data-ttu-id="b632f-116">En un entorno multilingüe, a veces se conocen los nombres localizados de los grupos integrados, lo que significa que no se pueden recuperar directamente mediante el uso de identificadores de cadena como "WinNT://Microsoft/Administrators".</span><span class="sxs-lookup"><span data-stu-id="b632f-116">In a multilingual environment, built-in groups are sometimes known by different localized names, which means that they cannot be retrieved directly by using string identifiers such as "WinNT://Microsoft/Administrators".</span></span> <span data-ttu-id="b632f-117">En ese caso, el usuario puede enlazar con el objeto de SID conocido del grupo, recuperar el nombre de grupo localizado y proporcionarlo al método GetObject.</span><span class="sxs-lookup"><span data-stu-id="b632f-117">In that case, the user can bind to the well-known SID object for the group, retrieve the localized group name, and supply that to the GetObject method.</span></span> <span data-ttu-id="b632f-118">Para obtener más información, vea [SID conocidos](/windows/desktop/SecAuthZ/well-known-sids).</span><span class="sxs-lookup"><span data-stu-id="b632f-118">For more information, see [Well-known SIDs](/windows/desktop/SecAuthZ/well-known-sids).</span></span>

## <a name="examples"></a><span data-ttu-id="b632f-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b632f-119">Examples</span></span>

<span data-ttu-id="b632f-120">En el siguiente Visual Basic ejemplo se muestra cómo enlazar a un objeto de grupo y mostrar la descripción del grupo.</span><span class="sxs-lookup"><span data-stu-id="b632f-120">The following Visual Basic example shows how to bind to a group object and display the description of the group.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="b632f-121">En el siguiente ejemplo de C++ se muestra cómo enlazar a un objeto de grupo y mostrar la descripción del grupo.</span><span class="sxs-lookup"><span data-stu-id="b632f-121">The following C++ example shows how to bind to a group object and display the description of the group.</span></span>


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a><span data-ttu-id="b632f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b632f-122">Requirements</span></span>



| <span data-ttu-id="b632f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b632f-123">Requirement</span></span> | <span data-ttu-id="b632f-124">Value</span><span class="sxs-lookup"><span data-stu-id="b632f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b632f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b632f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b632f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b632f-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b632f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b632f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b632f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b632f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b632f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b632f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b632f-130"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="b632f-130"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b632f-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b632f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b632f-132"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b632f-132"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b632f-133">IID</span><span class="sxs-lookup"><span data-stu-id="b632f-133">IID</span></span><br/>                      | <span data-ttu-id="b632f-134">IID \_ IADsGroup se define como 27636B00-410F-11cf-B1FF-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="b632f-134">IID\_IADsGroup is defined as 27636B00-410F-11CF-B1FF-02608C9E7553</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b632f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b632f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b632f-136">**IADs**</span><span class="sxs-lookup"><span data-stu-id="b632f-136">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="b632f-137">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="b632f-137">**IADsGroup**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="b632f-138">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="b632f-138">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

