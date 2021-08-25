---
description: Representa cualquier colección del catálogo de COM+. Úsese para enumerar, agregar, quitar y recuperar elementos de una colección y para acceder a colecciones relacionadas.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Clase COMAdminCatalogCollection (ComAdmin.h)
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
ms.openlocfilehash: 3656e65b89ae02b0cfe8ea3b1dbe9784d679c5eb40e11edbfe2951e08893e1aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029485"
---
# <a name="comadmincatalogcollection-class"></a>COMAdminCatalogCollection (clase)

Representa cualquier colección del catálogo de COM+. Úsese para enumerar, agregar, quitar y recuperar elementos de una colección y para acceder a colecciones relacionadas.

## <a name="when-to-implement"></a>Cuándo implementar

COM+implementa esta clase.



| Requisito | Value |
|------------|--------------------------------------------------|
| Interfaces | [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Cuándo se usa

Use objetos creados a partir **de la clase COMAdminCatalogCollection** cuando desee manipular mediante programación una colección en el catálogo de COM+. Estas colecciones corresponden a carpetas de la herramienta de administración servicios de componentes. Los elementos dentro de las carpetas corresponden a los elementos de las colecciones, que se pueden representar mediante objetos creados a partir de la [**clase COMAdminCatalogObject.**](comadmincatalogobject.md)

Para obtener información sobre las colecciones del catálogo y sus propiedades, vea [Colecciones de administración de COM+.](com--administration-collections.md)

Para obtener una introducción a la administración mediante programación de COM+, vea [Automatización de la administración de COM+.](automating-com--administration.md)

## <a name="remarks"></a>Comentarios

No se puede crear directamente **un objeto COMAdminCatalogCollection.** Para usar los métodos de este objeto, debe crear un objeto [**COMAdminCatalog,**](comadmincatalog.md) obtener una referencia a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)y, a continuación, usar [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obtener una referencia a una interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa una colección de nivel superior. Esto se muestra en el ejemplo siguiente, donde "TopCollection" debe reemplazarse por el nombre de una de las colecciones de administración de COM+ de nivel superior.


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



Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administrador de COM+. Se puede crear un objeto COMAdminCatalogCollection llamando a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en un [**objeto COMAdminCatalog.**](comadmincatalog.md) Esto se muestra en el ejemplo siguiente, donde "TopCollection" debe reemplazarse por el nombre de una de las colecciones de administración de COM+ de nivel superior.


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
| Encabezado<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.Idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




