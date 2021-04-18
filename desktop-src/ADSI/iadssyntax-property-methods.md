---
title: Métodos de la propiedad IADsSyntax (iAds. h)
description: Los métodos de propiedad de la interfaz IADsSyntax obtienen o establecen las propiedades enumeradas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsSyntax ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534042"
---
# <a name="iadssyntax-property-methods"></a><span data-ttu-id="d0735-105">Métodos de propiedad IADsSyntax</span><span class="sxs-lookup"><span data-stu-id="d0735-105">IADsSyntax Property Methods</span></span>

<span data-ttu-id="d0735-106">Los métodos de propiedad de la interfaz [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) obtienen o establecen las propiedades enumeradas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d0735-106">The property methods of the [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="d0735-107">Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d0735-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d0735-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0735-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d0735-109">**OleAutoDataType**</span><span class="sxs-lookup"><span data-stu-id="d0735-109">**OleAutoDataType**</span></span>
<span data-ttu-id="d0735-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d0735-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d0735-111">Recupera y establece un valor de **tipo Long** que contiene el valor de la constante **VT \_ XXX** para el tipo de datos de Automation que representa esta sintaxis.</span><span class="sxs-lookup"><span data-stu-id="d0735-111">Retrieves and sets a **LONG** that contains the value of the **VT\_xxx** constant for the Automation data type that represents this syntax.</span></span>

<span data-ttu-id="d0735-112">Active Directory admite las siguientes constantes **VT \_ XXX** para el tipo de datos de Automation que representa esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="d0735-112">Active Directory supports the following **VT\_xxx** constants for the Automation data type that represents this syntax:</span></span>

-   <span data-ttu-id="d0735-113">**VT \_ BOOL** bool</span><span class="sxs-lookup"><span data-stu-id="d0735-113">**VT\_BOOL** BOOL</span></span>
-   <span data-ttu-id="d0735-114">**VT \_ BSTR BSTR**</span><span class="sxs-lookup"><span data-stu-id="d0735-114">**VT\_BSTR** BSTR</span></span>
-   <span data-ttu-id="d0735-115">**VT \_ BSTRT** BSTRT</span><span class="sxs-lookup"><span data-stu-id="d0735-115">**VT\_BSTRT** BSTRT</span></span>
-   <span data-ttu-id="d0735-116">**VT \_ moneda CY**</span><span class="sxs-lookup"><span data-stu-id="d0735-116">**VT\_CY** CURRENCY</span></span>
-   <span data-ttu-id="d0735-117">**VT \_ Fecha de fecha**</span><span class="sxs-lookup"><span data-stu-id="d0735-117">**VT\_DATE** Date</span></span>
-   <span data-ttu-id="d0735-118">**VT \_** **null** vacío</span><span class="sxs-lookup"><span data-stu-id="d0735-118">**VT\_EMPTY** **NULL**</span></span>
-   <span data-ttu-id="d0735-119">**VT \_ ERROR** no válido</span><span class="sxs-lookup"><span data-stu-id="d0735-119">**VT\_ERROR** Not valid</span></span>
-   <span data-ttu-id="d0735-120">**VT \_ De i2** corto</span><span class="sxs-lookup"><span data-stu-id="d0735-120">**VT\_I2** short</span></span>
-   <span data-ttu-id="d0735-121">**VT \_ I4** Long</span><span class="sxs-lookup"><span data-stu-id="d0735-121">**VT\_I4** long</span></span>
-   <span data-ttu-id="d0735-122">**VT \_ R4** real</span><span class="sxs-lookup"><span data-stu-id="d0735-122">**VT\_R4** real</span></span>
-   <span data-ttu-id="d0735-123">**VT \_ R8** doble</span><span class="sxs-lookup"><span data-stu-id="d0735-123">**VT\_R8** double</span></span>
-   <span data-ttu-id="d0735-124">**VT \_ UI1** byte</span><span class="sxs-lookup"><span data-stu-id="d0735-124">**VT\_UI1** BYTE</span></span>

<dt>

<span data-ttu-id="d0735-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0735-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d0735-126">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d0735-126">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="d0735-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0735-127">Remarks</span></span>

<span data-ttu-id="d0735-128">Una matriz de bytes sin signo, la **matriz VT \_ UI1** \| **VT \_** podría significar que el proveedor ha asignado una sintaxis que no se puede asignar a un tipo virtual de automatización.</span><span class="sxs-lookup"><span data-stu-id="d0735-128">An array of unsigned bytes, **VT\_UI1**\|**VT\_ARRAY** could mean that the provider has mapped a syntax that cannot be mapped to an Automation virtual type.</span></span>

## <a name="examples"></a><span data-ttu-id="d0735-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d0735-129">Examples</span></span>

<span data-ttu-id="d0735-130">En el ejemplo de código siguiente se examina la sintaxis del atributo **OperatingSystemVersion** de un equipo en una red a través del proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="d0735-130">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="d0735-131">La sintaxis del resultado es una cadena.</span><span class="sxs-lookup"><span data-stu-id="d0735-131">The result syntax is a string.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



<span data-ttu-id="d0735-132">En el ejemplo de código siguiente se examina la sintaxis del atributo **OperatingSystemVersion** de un equipo en una red a través del proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="d0735-132">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="d0735-133">La sintaxis del resultado es una cadena.</span><span class="sxs-lookup"><span data-stu-id="d0735-133">The result syntax is a string.</span></span> <span data-ttu-id="d0735-134">Por motivos de brevedad, se omite la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="d0735-134">For brevity, error checking is omitted.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a><span data-ttu-id="d0735-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0735-135">Requirements</span></span>



| <span data-ttu-id="d0735-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0735-136">Requirement</span></span> | <span data-ttu-id="d0735-137">Value</span><span class="sxs-lookup"><span data-stu-id="d0735-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0735-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0735-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d0735-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0735-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0735-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0735-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d0735-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0735-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0735-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0735-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0735-143"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0735-143"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d0735-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0735-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0735-145"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0735-145"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0735-146">IID</span><span class="sxs-lookup"><span data-stu-id="d0735-146">IID</span></span><br/>                      | <span data-ttu-id="d0735-147">IID \_ IADsSyntax se define como C8F93DD2-4AE0-11cf-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="d0735-147">IID\_IADsSyntax is defined as C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d0735-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0735-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0735-149">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="d0735-149">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="d0735-150">**IADsProperty**</span><span class="sxs-lookup"><span data-stu-id="d0735-150">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="d0735-151">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="d0735-151">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





