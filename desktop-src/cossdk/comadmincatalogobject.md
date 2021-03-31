---
description: Representa los elementos de las colecciones en el catálogo de COM+. Úselo para recuperar y modificar las propiedades expuestas por un elemento de una colección.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: Clase COMAdminCatalogObject (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 19fb873e29ad235b11dfe6e7a95b2ad47a8405b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153068"
---
# <a name="comadmincatalogobject-class"></a><span data-ttu-id="f6c93-104">Clase COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="f6c93-104">COMAdminCatalogObject class</span></span>

<span data-ttu-id="f6c93-105">Representa los elementos de las colecciones en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="f6c93-105">Represents items in collections in the COM+ catalog.</span></span> <span data-ttu-id="f6c93-106">Úselo para recuperar y modificar las propiedades expuestas por un elemento de una colección.</span><span class="sxs-lookup"><span data-stu-id="f6c93-106">Use it to retrieve and modify properties exposed by an item in a collection.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f6c93-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="f6c93-107">When to implement</span></span>

<span data-ttu-id="f6c93-108">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="f6c93-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="f6c93-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c93-109">Requirement</span></span> | <span data-ttu-id="f6c93-110">Value</span><span class="sxs-lookup"><span data-stu-id="f6c93-110">Value</span></span> |
|------------|------------------------------------------|
| <span data-ttu-id="f6c93-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f6c93-111">Interfaces</span></span> | [<span data-ttu-id="f6c93-112">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="f6c93-112">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a><span data-ttu-id="f6c93-113">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="f6c93-113">When to use</span></span>

<span data-ttu-id="f6c93-114">Use los objetos creados a partir de la clase **COMAdminCatalogObject** para modificar las propiedades de los elementos contenidos en las colecciones en el catálogo de com+.</span><span class="sxs-lookup"><span data-stu-id="f6c93-114">Use objects created from the **COMAdminCatalogObject** class to modify the properties of items contained in collections in the COM+ catalog.</span></span> <span data-ttu-id="f6c93-115">Estos elementos corresponden a los elementos que se muestran dentro de las carpetas en el árbol de consola de la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="f6c93-115">These items correspond to items shown inside folders in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="f6c93-116">Las carpetas de la herramienta de administración de servicios de componentes se corresponden con las recopilaciones del catálogo, que se pueden representar mediante los objetos creados a partir de la clase [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f6c93-116">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span>

<span data-ttu-id="f6c93-117">No todas las colecciones y elementos expuestos a través de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y **COMAdminCatalogObject** están disponibles en la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="f6c93-117">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and **COMAdminCatalogObject** are available in the Component Services administration tool.</span></span>

<span data-ttu-id="f6c93-118">Para obtener información sobre colecciones específicas y sus propiedades, consulte [colecciones de administración de com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="f6c93-118">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="f6c93-119">Para obtener una introducción a la administración mediante programación de COM+, vea [automatizar la administración de com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="f6c93-119">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c93-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6c93-120">Remarks</span></span>

<span data-ttu-id="f6c93-121">No se puede crear directamente un objeto **COMAdminCatalogObject** .</span><span class="sxs-lookup"><span data-stu-id="f6c93-121">You cannot directly create a **COMAdminCatalogObject** object.</span></span> <span data-ttu-id="f6c93-122">Para usar los métodos de este objeto, debe crear un objeto [**COMAdminCatalog**](comadmincatalog.md) , obtener una referencia a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)y, a continuación, usar [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obtener una referencia a una interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa una colección de nivel superior o usar [**ICatalogCollection:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) para tener acceso a colecciones que no son de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="f6c93-122">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection or use [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) to access collections that are not top-level.</span></span>

<span data-ttu-id="f6c93-123">Una vez que tenga una referencia a la interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) de la colección en la que está interesado, llame a [**ICatalogCollection::P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) para rellenar la colección con todos sus elementos.</span><span class="sxs-lookup"><span data-stu-id="f6c93-123">After you have a reference to the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface of the collection in which you are interested, call [**ICatalogCollection::Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) to populate the collection with all of its items.</span></span> <span data-ttu-id="f6c93-124">Itere por cada uno de los elementos de la colección mediante una llamada a [**ICatalogCollection:: get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) para obtener una referencia a cada interfaz [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="f6c93-124">Iterate through each of the items in the collection by calling [**ICatalogCollection::get\_Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) to get a reference to each [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span> <span data-ttu-id="f6c93-125">Cuando encuentre el elemento de interés, puede modificar las propiedades del elemento y salir de la iteración.</span><span class="sxs-lookup"><span data-stu-id="f6c93-125">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="f6c93-126">Si realiza cambios en los elementos de una colección, debe llamar a [**ICatalogCollection:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para guardar los cambios en el catálogo de com+.</span><span class="sxs-lookup"><span data-stu-id="f6c93-126">If you make any changes to any items in a collection, you must call [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="f6c93-127">Esto se muestra en el ejemplo siguiente, donde "cocollection" se debe reemplazar por el nombre de una de las colecciones de administración de COM+ de nivel superior; "ItemName" se debe reemplazar por el nombre del elemento que le interese; "PropertyName" se debe reemplazar por el nombre de la propiedad que se está modificando en el elemento; y varNewProp se deben reemplazar por una variante que contenga el nuevo valor para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f6c93-127">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and varNewProp must be replaced by a VARIANT that contains the new value for the property.</span></span>


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



<span data-ttu-id="f6c93-128">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+.</span><span class="sxs-lookup"><span data-stu-id="f6c93-128">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="f6c93-129">Se puede crear un objeto COMAdminCatalogCollection llamando a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en un objeto [**COMAdminCatalog**](comadmincatalog.md) o [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f6c93-129">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) or [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="f6c93-130">Llame al método [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para rellenar la colección con todos sus elementos.</span><span class="sxs-lookup"><span data-stu-id="f6c93-130">Call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object to populate the collection with all of its items.</span></span> <span data-ttu-id="f6c93-131">Recorrer en iteración cada uno de los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="f6c93-131">Iterate through each of the items in the collection.</span></span> <span data-ttu-id="f6c93-132">Cuando encuentre el elemento de interés, puede modificar las propiedades del elemento y salir de la iteración.</span><span class="sxs-lookup"><span data-stu-id="f6c93-132">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="f6c93-133">Si realiza cambios en los elementos de una colección, debe llamar al método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) del objeto **COMAdminCatalogCollection** para guardar los cambios en el catálogo de com+.</span><span class="sxs-lookup"><span data-stu-id="f6c93-133">If you make any changes to any items in a collection, you must call the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method of the **COMAdminCatalogCollection** object to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="f6c93-134">Esto se muestra en el ejemplo siguiente, donde "cocollection" se debe reemplazar por el nombre de una de las colecciones de administración de COM+ de nivel superior; "ItemName" se debe reemplazar por el nombre del elemento que le interese; "PropertyName" se debe reemplazar por el nombre de la propiedad que se está modificando en el elemento; y NewPropValue deben reemplazarse por el nuevo valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f6c93-134">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and NewPropValue must be replaced by the new value for the property.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

```



## <a name="requirements"></a><span data-ttu-id="f6c93-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6c93-135">Requirements</span></span>



| <span data-ttu-id="f6c93-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c93-136">Requirement</span></span> | <span data-ttu-id="f6c93-137">Value</span><span class="sxs-lookup"><span data-stu-id="f6c93-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c93-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6c93-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c93-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f6c93-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f6c93-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6c93-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c93-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6c93-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f6c93-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6c93-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c93-143"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6c93-143"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6c93-144">IDL</span><span class="sxs-lookup"><span data-stu-id="f6c93-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6c93-145"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6c93-145"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6c93-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6c93-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c93-147">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="f6c93-147">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="f6c93-148">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="f6c93-148">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="f6c93-149">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="f6c93-149">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




