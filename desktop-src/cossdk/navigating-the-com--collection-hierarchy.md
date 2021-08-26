---
description: Navegar por la jerarquía de colecciones com+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navegar por la jerarquía de colecciones com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef6f23cd9f584b6cbe496fe7122abfa9978cd25cb28d81a5c89782b718138be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070455"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Navegar por la jerarquía de colecciones com+

Algunas colecciones se pueden recuperar fácilmente mediante el [**método GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el [**objeto COMAdminCatalog.**](comadmincatalog.md) Este método recupera una colección de "nivel superior"; es decir, una colección como [**Applications**](applications.md), que se encuentra por sí misma y que es única y no se subsume lógicamente en otra colección.

Sin embargo, muchas colecciones se subsume lógicamente en otra colección porque contienen elementos que forman parte de una estructura más grande. Por ejemplo, la colección [**Components**](components.md) está suumida o relacionada con la colección [**Applications**](applications.md) porque contiene los componentes instalados en una aplicación COM+ determinada, que a su vez corresponde a un elemento de la colección **Applications.** Las colecciones relacionadas como esta no son únicas; hay una colección **Components para** cada aplicación distinta.

Por lo tanto, las colecciones se organizan en una estructura jerárquica que se corresponde de forma natural con las relaciones lógicas entre los elementos que contienen. Puede encontrar un diagrama de la jerarquía de recopilación en [Colecciones de administración de COM+.](com--administration-collections.md) Para muchos de los elementos que desea configurar mediante los objetos COMAdmin, debe navegar por alguna parte de la jerarquía de colecciones para recuperar el elemento adecuado.

Lo que esto significa en la práctica es que, si desea obtener un elemento en una colección relacionada, primero debe pasar por todas las colecciones necesarias de nivel superior, las colecciones de subsuming. Y para recuperar una colección relacionada, debe recuperar el elemento específico de la colección primaria con la que está relacionada la colección secundaria. Por ejemplo, si desea configurar un elemento correspondiente a un componente en una aplicación COM+ determinada, debe realizar los pasos siguientes:

1.  Obtenga la [**colección Aplicaciones**](applications.md) y recopila.
2.  Enumerar a través del contenido de la [**colección Aplicaciones**](applications.md) hasta llegar al elemento correspondiente a la aplicación COM+ correcta.
3.  Obtenga y rellene la [**colección Components**](components.md) para esa aplicación COM+ concreta.
4.  Enumerar el contenido de la colección [**Components**](components.md) hasta llegar al elemento correspondiente al componente correcto.

En el siguiente Visual Basic ejemplo de Microsoft se muestra cómo realizar los pasos anteriores:


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



En el ejemplo anterior se usan dos métodos **GetCollection** distintos. [**COMAdminCatalog**](comadmincatalog.md) expone el primero y se usa para obtener una colección de nivel superior, en este caso, "Applications". [**COMAdminCatalogCollection**](comadmincatalogcollection.md) expone la segunda colección y se usa para obtener una colección relacionada con la colección actual. indica con precisión qué colección desea pasando el nombre "Components" y el valor de la propiedad Key del objeto primario. El valor de la propiedad Key suele ser un nombre o un GUID que identifica de forma única el objeto. este valor se identifica en la documentación de cada colección.

En el caso más general, debe obtener colecciones relacionadas de forma iterativa en la jerarquía de recopilación hasta que recupere la colección que desee. Los pasos que seguiría seguirían el mismo modelo general, de forma repetitiva. Para obtener una lista completa de colecciones, vea [Colecciones de administración de COM+.](com--administration-collections.md)

En algunos casos, es posible que quiera usar un método abreviado la segunda vez que siga una ruta de acceso a través de la jerarquía de colecciones. Puede usar este método solo después de haber almacenado en caché todos los valores de clave que intervienen. Para obtener más información, [**vea ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Rellenar colecciones COM+](populating-com--collections.md)
</dt> <dt>

[Consulta de colecciones relacionadas disponibles](querying-for-available-related-collections.md)
</dt> <dt>

[Recuperar colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



