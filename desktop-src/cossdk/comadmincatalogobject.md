---
description: Representa los elementos de las colecciones del catálogo de COM+. Úsese para recuperar y modificar las propiedades expuestas por un elemento de una colección.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: Clase COMAdminCatalogObject (ComAdmin.h)
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
ms.openlocfilehash: bce57021774b3abc2f69a1120862912452629c3e70d9c8fd0ebcc5d39ce5203d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548592"
---
# <a name="comadmincatalogobject-class"></a>COMAdminCatalogObject (clase)

Representa los elementos de las colecciones del catálogo de COM+. Úsese para recuperar y modificar las propiedades expuestas por un elemento de una colección.

## <a name="when-to-implement"></a>Cuándo implementar

ESTA clase se implementa mediante COM+.



| Requisito | Valor |
|------------|------------------------------------------|
| Interfaces | [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Cuándo se usa

Use objetos creados a partir **de la clase COMAdminCatalogObject** para modificar las propiedades de los elementos contenidos en colecciones del catálogo de COM+. Estos elementos corresponden a elementos que se muestran dentro de carpetas en el árbol de consola de la herramienta de administración servicios de componentes. Las carpetas de la herramienta de administración Servicios de componentes corresponden a colecciones del catálogo, que puede representar mediante objetos creados a partir de la [**clase COMAdminCatalogCollection.**](comadmincatalogcollection.md)

No todas las colecciones y elementos expuestos a través de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y **COMAdminCatalogObject** están disponibles en la herramienta de administración servicios de componentes.

Para obtener información sobre colecciones específicas y sus propiedades, vea [Colecciones de administración de COM+.](com--administration-collections.md)

Para obtener una introducción a la administración mediante programación de COM+, vea [Automatización de la administración de COM+.](automating-com--administration.md)

## <a name="remarks"></a>Comentarios

No se puede crear directamente **un objeto COMAdminCatalogObject.** Para usar los métodos de este objeto, debe crear un objeto [**COMAdminCatalog,**](comadmincatalog.md) obtener una referencia a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)y, a continuación, usar [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obtener una referencia a una interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa una colección de nivel superior o usar [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) para acceder a colecciones que no son de nivel superior.

Una vez que tenga una referencia a la interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) de la colección en la que está interesado, llame a [**ICatalogCollection::P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) para rellenar la colección con todos sus elementos. Itera por cada uno de los elementos de la colección llamando a [**ICatalogCollection::get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) para obtener una referencia a cada [**interfaz ICatalogObject.**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) Cuando encuentre el elemento de interés, puede modificar las propiedades del elemento y salir de la iteración. Si realiza cambios en los elementos de una colección, debe llamar a [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para guardar los cambios en el catálogo de COM+.

Esto se muestra en el ejemplo siguiente, donde "TopCollection" debe reemplazarse por el nombre de una de las colecciones de administración de COM+ de nivel superior; "ItemName" debe reemplazarse por el nombre del elemento que le interesa. "PropertyName" debe reemplazarse por el nombre de la propiedad que se va a modificar en el elemento; y varNewProp deben reemplazarse por un variant que contenga el nuevo valor de la propiedad .


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



Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administrador de COM+. Se puede crear un objeto COMAdminCatalogCollection llamando a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en un objeto [**COMAdminCatalog**](comadmincatalog.md) o [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

Llame al [**método Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) del [**objeto COMAdminCatalogCollection**](comadmincatalogcollection.md) para rellenar la colección con todos sus elementos. Recorrer en iteración cada uno de los elementos de la colección. Cuando encuentre el elemento de interés, puede modificar las propiedades del elemento y salir de la iteración. Si realiza cambios en los elementos de una colección, debe llamar al método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) del objeto **COMAdminCatalogCollection** para guardar los cambios en el catálogo de COM+.

Esto se muestra en el ejemplo siguiente, donde "TopCollection" debe reemplazarse por el nombre de una de las colecciones de administración de COM+ de nivel superior; "ItemName" debe reemplazarse por el nombre del elemento que le interesa; "PropertyName" debe reemplazarse por el nombre de la propiedad que se va a modificar en el elemento; y NewPropValue deben reemplazarse por el nuevo valor de la propiedad .


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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.Idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




