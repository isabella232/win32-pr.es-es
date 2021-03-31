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
# <a name="comadmincatalogobject-class"></a>Clase COMAdminCatalogObject

Representa los elementos de las colecciones en el catálogo de COM+. Úselo para recuperar y modificar las propiedades expuestas por un elemento de una colección.

## <a name="when-to-implement"></a>Cuándo implementar

Esta clase se implementa mediante COM+.



| Requisito | Value |
|------------|------------------------------------------|
| Interfaces | [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Cuándo se usa

Use los objetos creados a partir de la clase **COMAdminCatalogObject** para modificar las propiedades de los elementos contenidos en las colecciones en el catálogo de com+. Estos elementos corresponden a los elementos que se muestran dentro de las carpetas en el árbol de consola de la herramienta de administración de servicios de componentes. Las carpetas de la herramienta de administración de servicios de componentes se corresponden con las recopilaciones del catálogo, que se pueden representar mediante los objetos creados a partir de la clase [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

No todas las colecciones y elementos expuestos a través de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y **COMAdminCatalogObject** están disponibles en la herramienta de administración de servicios de componentes.

Para obtener información sobre colecciones específicas y sus propiedades, consulte [colecciones de administración de com+](com--administration-collections.md).

Para obtener una introducción a la administración mediante programación de COM+, vea [automatizar la administración de com+](automating-com--administration.md).

## <a name="remarks"></a>Observaciones

No se puede crear directamente un objeto **COMAdminCatalogObject** . Para usar los métodos de este objeto, debe crear un objeto [**COMAdminCatalog**](comadmincatalog.md) , obtener una referencia a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)y, a continuación, usar [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obtener una referencia a una interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa una colección de nivel superior o usar [**ICatalogCollection:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) para tener acceso a colecciones que no son de nivel superior.

Una vez que tenga una referencia a la interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) de la colección en la que está interesado, llame a [**ICatalogCollection::P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) para rellenar la colección con todos sus elementos. Itere por cada uno de los elementos de la colección mediante una llamada a [**ICatalogCollection:: get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) para obtener una referencia a cada interfaz [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) . Cuando encuentre el elemento de interés, puede modificar las propiedades del elemento y salir de la iteración. Si realiza cambios en los elementos de una colección, debe llamar a [**ICatalogCollection:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para guardar los cambios en el catálogo de com+.

Esto se muestra en el ejemplo siguiente, donde "cocollection" se debe reemplazar por el nombre de una de las colecciones de administración de COM+ de nivel superior; "ItemName" se debe reemplazar por el nombre del elemento que le interese; "PropertyName" se debe reemplazar por el nombre de la propiedad que se está modificando en el elemento; y varNewProp se deben reemplazar por una variante que contenga el nuevo valor para la propiedad.


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



Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+. Se puede crear un objeto COMAdminCatalogCollection llamando a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en un objeto [**COMAdminCatalog**](comadmincatalog.md) o [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Llame al método [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para rellenar la colección con todos sus elementos. Recorrer en iteración cada uno de los elementos de la colección. Cuando encuentre el elemento de interés, puede modificar las propiedades del elemento y salir de la iteración. Si realiza cambios en los elementos de una colección, debe llamar al método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) del objeto **COMAdminCatalogCollection** para guardar los cambios en el catálogo de com+.

Esto se muestra en el ejemplo siguiente, donde "cocollection" se debe reemplazar por el nombre de una de las colecciones de administración de COM+ de nivel superior; "ItemName" se debe reemplazar por el nombre del elemento que le interese; "PropertyName" se debe reemplazar por el nombre de la propiedad que se está modificando en el elemento; y NewPropValue deben reemplazarse por el nuevo valor de la propiedad.


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>COMAdmin. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




