---
title: Métodos de la propiedad IADsResource (iAds. h)
description: Los métodos de propiedad de la interfaz IADsResource obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener una explicación general de los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsResource ADSI
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f2ab2642dd8d03062a26d096190cf7615977a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656530"
---
# <a name="iadsresource-property-methods"></a><span data-ttu-id="f46af-105">Métodos de propiedad IADsResource</span><span class="sxs-lookup"><span data-stu-id="f46af-105">IADsResource Property Methods</span></span>

<span data-ttu-id="f46af-106">Los métodos de propiedad de la interfaz [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f46af-106">The property methods of the [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="f46af-107">Para obtener una explicación general de los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f46af-107">For a general discussion of property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f46af-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f46af-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f46af-109">**LockCount**</span><span class="sxs-lookup"><span data-stu-id="f46af-109">**LockCount**</span></span>
<span data-ttu-id="f46af-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f46af-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f46af-111">Número de bloqueos en el recurso.</span><span class="sxs-lookup"><span data-stu-id="f46af-111">Number of locks on the resource.</span></span>

<dt>

<span data-ttu-id="f46af-112">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f46af-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f46af-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="f46af-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f46af-114">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="f46af-114">**Path**</span></span>
<span data-ttu-id="f46af-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f46af-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="f46af-116">Ruta de acceso del sistema de archivos del recurso abierto.</span><span class="sxs-lookup"><span data-stu-id="f46af-116">The file system path of the opened resource.</span></span>

<dt>

<span data-ttu-id="f46af-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f46af-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f46af-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f46af-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f46af-119">**User**</span><span class="sxs-lookup"><span data-stu-id="f46af-119">**User**</span></span>
<span data-ttu-id="f46af-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f46af-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="f46af-121">Nombre del usuario que abrió el recurso.</span><span class="sxs-lookup"><span data-stu-id="f46af-121">The name of the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="f46af-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f46af-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f46af-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f46af-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f46af-124">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="f46af-124">**UserPath**</span></span>
<span data-ttu-id="f46af-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f46af-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="f46af-126">ADsPath del objeto de usuario para el usuario que abrió el recurso.</span><span class="sxs-lookup"><span data-stu-id="f46af-126">The ADsPath of the user object for the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="f46af-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f46af-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f46af-128">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f46af-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="f46af-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f46af-129">Examples</span></span>

<span data-ttu-id="f46af-130">En el ejemplo de código siguiente se muestra cómo examinar los recursos abiertos de un servicio de archivos.</span><span class="sxs-lookup"><span data-stu-id="f46af-130">The following code example shows how to examine open resources of a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="f46af-131">En el ejemplo de código siguiente se enumera una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="f46af-131">The following code example enumerates a collection of resources.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a><span data-ttu-id="f46af-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f46af-132">Requirements</span></span>



| <span data-ttu-id="f46af-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f46af-133">Requirement</span></span> | <span data-ttu-id="f46af-134">Value</span><span class="sxs-lookup"><span data-stu-id="f46af-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f46af-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f46af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f46af-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f46af-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f46af-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f46af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f46af-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f46af-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f46af-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f46af-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f46af-140"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="f46af-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f46af-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f46af-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f46af-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f46af-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f46af-143">IID</span><span class="sxs-lookup"><span data-stu-id="f46af-143">IID</span></span><br/>                      | <span data-ttu-id="f46af-144">IID \_ IADsResource se define como 34A05B20-4AAB-11cf-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="f46af-144">IID\_IADsResource is defined as 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="f46af-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f46af-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f46af-146">**IADsResource**</span><span class="sxs-lookup"><span data-stu-id="f46af-146">**IADsResource**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[<span data-ttu-id="f46af-147">**IADsFileServiceOperations:: Resources**</span><span class="sxs-lookup"><span data-stu-id="f46af-147">**IADsFileServiceOperations::Resources**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 





