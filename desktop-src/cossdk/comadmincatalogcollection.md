---
description: Representa cualquier colección en el catálogo de COM+. Úselo para enumerar, agregar, quitar y recuperar elementos de una colección y para obtener acceso a colecciones relacionadas.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Clase COMAdminCatalogCollection (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807646"
---
# <a name="comadmincatalogcollection-class"></a>Clase COMAdminCatalogCollection

Representa cualquier colección en el catálogo de COM+. Úselo para enumerar, agregar, quitar y recuperar elementos de una colección y para obtener acceso a colecciones relacionadas.

## <a name="when-to-implement"></a>Cuándo implementar

Esta clase se implementa mediante COM+.



| Requisito | Value |
|------------|--------------------------------------------------|
| Interfaces | [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Cuándo se usa

Utilice los objetos creados a partir de la clase **COMAdminCatalogCollection** cuando desee manipular mediante programación una colección en el catálogo de com+. Estas colecciones corresponden a las carpetas de la herramienta de administración de servicios de componentes. Los elementos de las carpetas se corresponden con los elementos de las colecciones, que puede representar con los objetos creados a partir de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Para obtener información sobre las colecciones en el catálogo y sus propiedades, consulte [colecciones de administración de com+](com--administration-collections.md).

Para obtener una introducción a la administración mediante programación de COM+, vea [automatizar la administración de com+](automating-com--administration.md).

## <a name="remarks"></a>Observaciones

No se puede crear directamente un objeto **COMAdminCatalogCollection** . Para usar los métodos de este objeto, debe crear un objeto [**COMAdminCatalog**](comadmincatalog.md) , obtener una referencia a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)y, a continuación, usar [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obtener una referencia a una interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa una colección de nivel superior. Esto se muestra en el ejemplo siguiente, donde "cocollection" se debe reemplazar por el nombre de una de las colecciones de administración de COM+ de nivel superior.


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+. Se puede crear un objeto COMAdminCatalogCollection llamando a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en un objeto [**COMAdminCatalog**](comadmincatalog.md) . Esto se muestra en el ejemplo siguiente, donde "cocollection" se debe reemplazar por el nombre de una de las colecciones de administración de COM+ de nivel superior.


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

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

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




