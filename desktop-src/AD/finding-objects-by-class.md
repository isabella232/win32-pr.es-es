---
title: Buscar objetos por clase
description: Una consulta de búsqueda típica para una clase de objeto específica.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Buscar objetos por clase AD
- Active Directory, usar, buscar, por clase
- object AD , buscando por clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81d90dbcd50a3ce001c1dec57d8fafb0f1987376cf71314902b7f035f923512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189175"
---
# <a name="finding-objects-by-class"></a>Buscar objetos por clase

Una consulta de búsqueda típica para una clase de objeto específica. En el ejemplo de código siguiente se buscan equipos con ubicación en Building 7N.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Tenga en cuenta **por qué no** se usa objectClass. No use **objectClass** sin otra comparación que contenga un atributo indizado. Los atributos de índice pueden aumentar la eficacia de una consulta. El **atributo objectClass** tiene varios valores y no está indexado. Para especificar el tipo o clase de un objeto, use **objectCategory**.

Menos eficaz:


```C++
(objectClass=computer)
```



Más eficaz:


```C++
(objectCategory=computer)
```



Tenga en cuenta que hay algunos casos en los que se debe usar una combinación de **objectClass** y **objectCategory.** La clase de usuario y la clase de contacto deben especificarse como se indica a continuación.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



Tenga en cuenta que puede buscar usuarios y contactos con lo siguiente.


```C++
(objectCategory=person)
```



 

 




