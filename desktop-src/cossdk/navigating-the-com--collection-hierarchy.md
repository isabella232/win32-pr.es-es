---
description: Navegar por la jerarquía de la colección de COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navegar por la jerarquía de la colección de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677218"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Navegar por la jerarquía de la colección de COM+

Algunas colecciones se pueden recuperar fácilmente mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el objeto [**COMAdminCatalog**](comadmincatalog.md) . Este método recupera una colección "de nivel superior"; es decir, una colección como [**aplicaciones**](applications.md), que se sitúa por sí misma y que es única y no se encuentra lógicamente en otra colección.

Sin embargo, muchas colecciones se integran lógicamente en otra colección porque contienen elementos que forman parte de una estructura mayor. Por ejemplo, la colección de [**componentes**](components.md) se incluye o se relaciona en la colección de [**aplicaciones**](applications.md) porque contiene los componentes instalados en una aplicación com+ determinada, que se corresponde con un elemento de la colección de **aplicaciones** . Las colecciones relacionadas como esta no son únicas; hay una colección de **componentes** para cada aplicación distinta.

Por lo tanto, las colecciones se organizan en una estructura jerárquica que corresponde de forma natural a las relaciones lógicas entre los elementos que contienen. Puede encontrar un diagrama de la jerarquía de la colección en [colecciones de administración de com+](com--administration-collections.md). Para muchos de los elementos que desea configurar mediante los objetos COMAdmin, debe desplazarse por una parte de la jerarquía de la colección para recuperar el elemento adecuado.

Esto significa que, en la práctica, si desea obtener un elemento en una colección relacionada, debe repasar en primer lugar todas las colecciones de nivel superior necesarias, integrador indicado. Y para recuperar una colección relacionada, debe recuperar el elemento específico en la colección primaria en la que está relacionada la colección secundaria. Por ejemplo, si desea configurar un elemento correspondiente a un componente de una aplicación COM+ determinada, debe realizar los siguientes pasos:

1.  Obtener la colección de [**aplicaciones**](applications.md) y rellenarla.
2.  Enumere el contenido de la colección de [**aplicaciones**](applications.md) hasta llegar al elemento correspondiente a la aplicación com+ correcta.
3.  Obtener y rellenar la colección de [**componentes**](components.md) para esa aplicación com+ en particular.
4.  Enumere el contenido de la colección de [**componentes**](components.md) hasta llegar al elemento correspondiente al componente correcto.

En el siguiente ejemplo de Microsoft Visual Basic se muestra cómo realizar los pasos anteriores:


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



En el ejemplo anterior se usan dos métodos **GetCollection** distintos. La primera se expone mediante [**COMAdminCatalog**](comadmincatalog.md) y se usa para obtener una colección de nivel superior (en este caso, "Applications"). La segunda se expone mediante [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y se usa para obtener una colección relacionada con la colección actual; para indicar exactamente qué colección desea, pase el nombre "Components" y el valor de la propiedad clave del objeto primario. El valor de la propiedad clave suele ser un nombre o un GUID que identifica de forma única el objeto. Este valor se identifica en la documentación de cada colección.

En el caso más general, debe obtener las colecciones relacionadas de forma iterativa hacia abajo en la jerarquía de la colección hasta que recupere la colección que desea. Los pasos que debería seguir el mismo modelo general, repetidamente. Para obtener una lista completa de las colecciones, consulte [colecciones de administración de com+](com--administration-collections.md).

En algunos casos, es posible que desee usar un método abreviado la segunda vez que siga una ruta de acceso a través de la jerarquía de la colección. Puede usar este método solo después de haber almacenado en caché todos los valores de clave que intervienen. Para obtener más información, vea [**ICOMAdminCatalog:: GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Rellenar colecciones de COM+](populating-com--collections.md)
</dt> <dt>

[Consultar colecciones relacionadas disponibles](querying-for-available-related-collections.md)
</dt> <dt>

[Recuperar recopilaciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



