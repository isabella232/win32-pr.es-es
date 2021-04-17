---
title: Métodos de la propiedad IADsProperty (iAds. h)
description: Lea y escriba las propiedades descritas en la tabla siguiente.
ms.assetid: dd348a3c-0386-4fa2-984d-cdea6f09bd72
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsProperty ADSI
topic_type:
- apiref
api_name:
- IADsProperty Property Methods
- IADsProperty.OID
- IADsProperty.get_OID
- IADsProperty.put_OID
- IADsProperty.Syntax
- IADsProperty.get_Syntax
- IADsProperty.put_Syntax
- IADsProperty.MaxRange
- IADsProperty.get_MaxRange
- IADsProperty.put_MaxRange
- IADsProperty.MinRange
- IADsProperty.get_MinRange
- IADsProperty.put_MinRange
- IADsProperty.MultiValued
- IADsProperty.get_MultiValued
- IADsProperty.put_MultiValued
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233bd5411e1c82956ef745255418a1b176af5900
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656479"
---
# <a name="iadsproperty-property-methods"></a><span data-ttu-id="a22c7-104">Métodos de propiedad IADsProperty</span><span class="sxs-lookup"><span data-stu-id="a22c7-104">IADsProperty Property Methods</span></span>

<span data-ttu-id="a22c7-105">Los métodos de propiedad de la interfaz [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) leen y escriben las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a22c7-105">The property methods of the [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interface read and write the properties described in the following table.</span></span> <span data-ttu-id="a22c7-106">Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a22c7-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a22c7-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a22c7-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="a22c7-108">**MaxRange**</span><span class="sxs-lookup"><span data-stu-id="a22c7-108">**MaxRange**</span></span>
<span data-ttu-id="a22c7-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a22c7-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="a22c7-110">Límite superior de valores.</span><span class="sxs-lookup"><span data-stu-id="a22c7-110">Upper limit of values.</span></span>

<dt>

<span data-ttu-id="a22c7-111">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22c7-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a22c7-112">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="a22c7-112">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxRange(
  [out] LONG* lnMaxRange
);
HRESULT put_MaxRange(
  [in] LONG lnMaxRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a22c7-113">**MinRange**</span><span class="sxs-lookup"><span data-stu-id="a22c7-113">**MinRange**</span></span>
<span data-ttu-id="a22c7-114"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a22c7-114"></dt> <dd> <dl></span></span>

<span data-ttu-id="a22c7-115">Límite inferior de valores.</span><span class="sxs-lookup"><span data-stu-id="a22c7-115">Lower limit of values.</span></span>

<dt>

<span data-ttu-id="a22c7-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22c7-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a22c7-117">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="a22c7-117">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinRange(
  [out] LONG* lnMinRange
);
HRESULT put_MinRange(
  [in] LONG lnMinRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a22c7-118">**Varios valores**</span><span class="sxs-lookup"><span data-stu-id="a22c7-118">**MultiValued**</span></span>
<span data-ttu-id="a22c7-119"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a22c7-119"></dt> <dd> <dl></span></span>

<span data-ttu-id="a22c7-120">Indica si la propiedad admite uno o varios valores.</span><span class="sxs-lookup"><span data-stu-id="a22c7-120">Whether property supports single or multiple values.</span></span>

<dt>

<span data-ttu-id="a22c7-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22c7-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a22c7-122">Tipo de datos de scripting: **variante \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a22c7-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MultiValued(
  [out] VARIANT_BOOL* fMultivalued
);
HRESULT put_MultiValued(
  [in] VARIANT_BOOL fMultivalued
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a22c7-123">**OID**</span><span class="sxs-lookup"><span data-stu-id="a22c7-123">**OID**</span></span>
<span data-ttu-id="a22c7-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a22c7-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="a22c7-125">Identificador de objeto específico del directorio.</span><span class="sxs-lookup"><span data-stu-id="a22c7-125">Directory-specific object identifier.</span></span>

<dt>

<span data-ttu-id="a22c7-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22c7-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a22c7-127">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a22c7-127">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* bstrOID
);
HRESULT put_OID(
  [out] BSTR* bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a22c7-128">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="a22c7-128">**Syntax**</span></span>
<span data-ttu-id="a22c7-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a22c7-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="a22c7-130">Ruta de acceso relativa del objeto de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="a22c7-130">Relative path of syntax object.</span></span>

<dt>

<span data-ttu-id="a22c7-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22c7-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a22c7-132">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a22c7-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Syntax(
  [out] BSTR* bstrSyntax
);
HRESULT put_Syntax(
  [in] BSTR* bstrSyntax
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="a22c7-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a22c7-133">Examples</span></span>

<span data-ttu-id="a22c7-134">En el ejemplo de código siguiente se examina el atributo **OperatingSystem** de un equipo en una red a través del proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="a22c7-134">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sc As IADsContainer

On Error GoTo Cleanup
 
Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystem")
 
MsgBox "Attribute:  " & pr.Name
MsgBox "Syntax:     " & pr.Syntax
MsgBox "MaxRange:   " & pr.MaxRange
MsgBox "MinRange:   " & pr.MinRange
MsgBox "Multivalued:" & pr.Multivalued

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sc = Nothing
```



<span data-ttu-id="a22c7-135">En el ejemplo de código siguiente se examina el atributo **OperatingSystem** de un equipo en una red a través del proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="a22c7-135">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="a22c7-136">Por motivos de brevedad, se omite la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="a22c7-136">For brevity, error checking is omitted.</span></span>


```C++
IADs *pADs = NULL;
IADsClass *pCls = NULL;
IADsProperty* pProp = NULL;
IADsContainer *pCont = NULL;
long lval;
short bval;
HRESULT hr = CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine,computer",
                  IID_IADs, (void**)&pADs);
if(FAILED(hr))
    goto Cleanup;

BSTR bstr;
hr = pADs->get_Schema(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsClass, (void**)&pCls);
hr = pCls->get_Parent(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr))
    goto Cleanup;
SysFreeString(bstr);

hr = pCont->GetObject(CComBSTR("Property"), CComBSTR("OperatingSystem"), (IDispatch**)&pProp);
if(FAILED(hr))
    goto Cleanup;

hr = pProp->get_Name(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Name : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_Syntax(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Syntax : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_MaxRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MaxRange : %d\n",lval);
SysFreeString(bstr);

hr = pProp->get_MinRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MinRange : %d\n", lval);
SysFreeString(bstr);

hr = pProp->get_Multivalued(&bval);
if(FAILED(hr))
    goto Cleanup;
printf(" MultiValued : %b\n",bval);
SysFreeString(bstr);

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    if(pCont)
        pCont->Release();

    if(pProp)
        pProp->Release(); 
 
CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="a22c7-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a22c7-137">Requirements</span></span>



| <span data-ttu-id="a22c7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22c7-138">Requirement</span></span> | <span data-ttu-id="a22c7-139">Value</span><span class="sxs-lookup"><span data-stu-id="a22c7-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a22c7-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a22c7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a22c7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a22c7-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a22c7-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a22c7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a22c7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a22c7-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a22c7-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a22c7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a22c7-145"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="a22c7-145"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="a22c7-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a22c7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22c7-147"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22c7-147"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="a22c7-148">IID</span><span class="sxs-lookup"><span data-stu-id="a22c7-148">IID</span></span><br/>                      | <span data-ttu-id="a22c7-149">IID \_ IADsProperty se define como C8F93DD3-4AE0-11cf-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="a22c7-149">IID\_IADsProperty is defined as C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="a22c7-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="a22c7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22c7-151">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="a22c7-151">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="a22c7-152">**IADsProperty**</span><span class="sxs-lookup"><span data-stu-id="a22c7-152">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="a22c7-153">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="a22c7-153">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





