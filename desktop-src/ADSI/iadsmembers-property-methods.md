---
title: Métodos de la propiedad IADsMembers (iAds. h)
description: Los métodos de la interfaz IADsMembers leen y escriben las propiedades descritas en este tema. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsMembers ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658301"
---
# <a name="iadsmembers-property-methods"></a><span data-ttu-id="1c3aa-105">Métodos de propiedad IADsMembers</span><span class="sxs-lookup"><span data-stu-id="1c3aa-105">IADsMembers Property Methods</span></span>

<span data-ttu-id="1c3aa-106">Los métodos de la interfaz [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) leen y escriben las propiedades descritas en este tema.</span><span class="sxs-lookup"><span data-stu-id="1c3aa-106">The methods of the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="1c3aa-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1c3aa-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1c3aa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c3aa-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="1c3aa-109">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="1c3aa-109">**Count**</span></span>
<span data-ttu-id="1c3aa-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1c3aa-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="1c3aa-111">Indica el número de elementos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="1c3aa-111">Indicates the number of items in the container.</span></span> <span data-ttu-id="1c3aa-112">Si se establece el filtro, Count solo devuelve el número de elementos que se ajustan a la descripción del filtro.</span><span class="sxs-lookup"><span data-stu-id="1c3aa-112">If the filter is set then count returns only the number of items that fit the filter description.</span></span>

<dt>

<span data-ttu-id="1c3aa-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1c3aa-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c3aa-114">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="1c3aa-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c3aa-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="1c3aa-115">**Filter**</span></span>
<span data-ttu-id="1c3aa-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1c3aa-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="1c3aa-117">Indica el filtro.</span><span class="sxs-lookup"><span data-stu-id="1c3aa-117">Indicates the filter.</span></span> <span data-ttu-id="1c3aa-118">La sintaxis de las entradas de la matriz de filtros es la misma que la del filtro utilizado en la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="1c3aa-118">The syntax of the entries in the filter array is the same as the Filter used on the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span>

<dt>

<span data-ttu-id="1c3aa-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c3aa-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1c3aa-120">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="1c3aa-120">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="1c3aa-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c3aa-121">Remarks</span></span>

<span data-ttu-id="1c3aa-122">Los proveedores del sistema ADSI no admiten el método de propiedad **IADsMembers:: get \_ Count** .</span><span class="sxs-lookup"><span data-stu-id="1c3aa-122">The ADSI system providers do not support the **IADsMembers::get\_Count** property method.</span></span>

## <a name="examples"></a><span data-ttu-id="1c3aa-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1c3aa-123">Examples</span></span>

<span data-ttu-id="1c3aa-124">En el ejemplo de código siguiente se muestra cómo utilizar los métodos de propiedad de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="1c3aa-124">The following code example shows how to use the property methods of this interface.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="1c3aa-125">En el ejemplo de código siguiente se usa el método de **\_ filtro IADsMembers::p UT** para preparar una enumeración de la colección de miembros de un grupo.</span><span class="sxs-lookup"><span data-stu-id="1c3aa-125">The following code example uses the **IADsMembers::put\_Filter** method to prepare for an enumeration of the collection of members of a group.</span></span>


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="1c3aa-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c3aa-126">Requirements</span></span>



| <span data-ttu-id="1c3aa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c3aa-127">Requirement</span></span> | <span data-ttu-id="1c3aa-128">Value</span><span class="sxs-lookup"><span data-stu-id="1c3aa-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c3aa-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c3aa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1c3aa-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c3aa-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c3aa-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c3aa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1c3aa-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c3aa-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c3aa-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c3aa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c3aa-134"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c3aa-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="1c3aa-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c3aa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c3aa-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c3aa-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c3aa-137">IID</span><span class="sxs-lookup"><span data-stu-id="1c3aa-137">IID</span></span><br/>                      | <span data-ttu-id="1c3aa-138">IID \_ IADsMembers se define como 451A0030-72EC-11cf-B03B-00AA006E0975</span><span class="sxs-lookup"><span data-stu-id="1c3aa-138">IID\_IADsMembers is defined as 451A0030-72EC-11CF-B03B-00AA006E0975</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1c3aa-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c3aa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c3aa-140">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="1c3aa-140">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="1c3aa-141">**IADsMembers:: get \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="1c3aa-141">**IADsMembers::get\_\_NewEnum**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[<span data-ttu-id="1c3aa-142">**IADsMembers**</span><span class="sxs-lookup"><span data-stu-id="1c3aa-142">**IADsMembers**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[<span data-ttu-id="1c3aa-143">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="1c3aa-143">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





