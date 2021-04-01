---
title: Métodos de propiedad IADsContainer (iAds. h)
description: Los métodos de propiedad de la interfaz IADsContainer obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información y una explicación general sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad de IADsContainer ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150776"
---
# <a name="iadscontainer-property-methods"></a><span data-ttu-id="75ea0-105">Métodos de propiedad de IADsContainer</span><span class="sxs-lookup"><span data-stu-id="75ea0-105">IADsContainer Property Methods</span></span>

<span data-ttu-id="75ea0-106">Los métodos de propiedad de la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="75ea0-106">The property methods of the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="75ea0-107">Para obtener más información y una explicación general sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="75ea0-107">For more information, and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="75ea0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75ea0-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="75ea0-109">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="75ea0-109">**Count**</span></span>
<span data-ttu-id="75ea0-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75ea0-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="75ea0-111">Recupera el número de elementos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="75ea0-111">Retrieves the number of items in the container.</span></span> <span data-ttu-id="75ea0-112">Cuando se establece **Filter** , **Count** solo devuelve el número de elementos filtrados.</span><span class="sxs-lookup"><span data-stu-id="75ea0-112">When **Filter** is set, **Count** returns only the number of filtered items.</span></span>

<dt>

<span data-ttu-id="75ea0-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="75ea0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75ea0-114">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="75ea0-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="75ea0-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="75ea0-115">**Filter**</span></span>
<span data-ttu-id="75ea0-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75ea0-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="75ea0-117">Recupera o establece el filtro que se usa para seleccionar las clases de objeto en una enumeración determinada.</span><span class="sxs-lookup"><span data-stu-id="75ea0-117">Retrieves or sets the filter used to select object classes in a given enumeration.</span></span> <span data-ttu-id="75ea0-118">Se trata de una matriz de tipo Variant, donde cada elemento es el nombre de una clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="75ea0-118">This is a variant array, each element of which is the name of a schema class.</span></span> <span data-ttu-id="75ea0-119">Si **Filter** no se establece o se establece en Empty, el enumerador recupera todos los objetos de todas las clases.</span><span class="sxs-lookup"><span data-stu-id="75ea0-119">If **Filter** is not set or set to empty, all objects of all classes are retrieved by the enumerator.</span></span>

<dt>

<span data-ttu-id="75ea0-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75ea0-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75ea0-121">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="75ea0-121">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="75ea0-122">**Sugerencias**</span><span class="sxs-lookup"><span data-stu-id="75ea0-122">**Hints**</span></span>
<span data-ttu-id="75ea0-123"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="75ea0-123"></dt> <dd> <dl></span></span>

<span data-ttu-id="75ea0-124">Matriz de variantes de cadenas **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="75ea0-124">A variant array of **BSTR** strings.</span></span> <span data-ttu-id="75ea0-125">Cada elemento identifica el nombre de una propiedad que se encuentra en la definición del esquema.</span><span class="sxs-lookup"><span data-stu-id="75ea0-125">Each element identifies the name of a property found in the schema definition.</span></span> <span data-ttu-id="75ea0-126">El parámetro *vHints* permite al cliente indicar qué atributos se van a cargar para cada objeto enumerado.</span><span class="sxs-lookup"><span data-stu-id="75ea0-126">The *vHints* parameter enables the client to indicate which attributes to load for each enumerated object.</span></span> <span data-ttu-id="75ea0-127">Estos datos se pueden usar para optimizar el acceso a la red.</span><span class="sxs-lookup"><span data-stu-id="75ea0-127">Such data may be used to optimize network access.</span></span> <span data-ttu-id="75ea0-128">Sin embargo, la implementación exacta es específica del proveedor y el proveedor de WinNT no la usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="75ea0-128">The exact implementation, however, is provider-specific, and is currently not used by the WinNT provider.</span></span>

<dt>

<span data-ttu-id="75ea0-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75ea0-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75ea0-130">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="75ea0-130">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="75ea0-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75ea0-131">Remarks</span></span>

<span data-ttu-id="75ea0-132">Los procesos de enumeración en [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) y **IADsContainer: \_ : get** se realizan en los objetos contenidos en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="75ea0-132">The enumeration processes under [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) and **IADsContainer::get\_Count** are performed against the contained objects in the cache.</span></span> <span data-ttu-id="75ea0-133">Cuando un contenedor contiene un gran número de objetos, el rendimiento puede verse afectado.</span><span class="sxs-lookup"><span data-stu-id="75ea0-133">When a container contains a large number of objects, the performance may be affected.</span></span> <span data-ttu-id="75ea0-134">Para mejorar el rendimiento, desactive la memoria caché, configure un tamaño de página adecuado y use la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="75ea0-134">To enhance performance, turn off the cache, set up an appropriate page size, and use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="75ea0-135">Por esta razón, la propiedad **Get \_ Count** no se admite en el proveedor LDAP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="75ea0-135">For this reason, the **get\_Count** property is not supported in the Microsoft LDAP provider.</span></span>

## <a name="examples"></a><span data-ttu-id="75ea0-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="75ea0-136">Examples</span></span>

<span data-ttu-id="75ea0-137">En el siguiente ejemplo de código Visual Basic se muestra cómo se pueden utilizar los métodos de propiedad de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="75ea0-137">The following Visual Basic code example shows how property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span>


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



<span data-ttu-id="75ea0-138">En el ejemplo de código de C++ siguiente se muestra cómo se pueden utilizar los métodos de propiedad de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="75ea0-138">The following C++ code example shows how the property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span> <span data-ttu-id="75ea0-139">Por motivos de brevedad, se omite la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="75ea0-139">For brevity, error checking is omitted.</span></span>


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="75ea0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75ea0-140">Requirements</span></span>



| <span data-ttu-id="75ea0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ea0-141">Requirement</span></span> | <span data-ttu-id="75ea0-142">Value</span><span class="sxs-lookup"><span data-stu-id="75ea0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75ea0-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75ea0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="75ea0-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75ea0-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75ea0-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75ea0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="75ea0-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75ea0-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75ea0-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75ea0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ea0-148"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="75ea0-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="75ea0-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75ea0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75ea0-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75ea0-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="75ea0-151">IID</span><span class="sxs-lookup"><span data-stu-id="75ea0-151">IID</span></span><br/>                      | <span data-ttu-id="75ea0-152">IID \_ IADsContainer se define como 001677D0-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="75ea0-152">IID\_IADsContainer is defined as 001677D0-FD16-11CE-ABC4-02608C9E7553</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="75ea0-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="75ea0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ea0-154">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="75ea0-154">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="75ea0-155">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="75ea0-155">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





