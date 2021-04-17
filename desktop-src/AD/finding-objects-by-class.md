---
title: Buscar objetos por clase
description: Consulta de búsqueda típica para una clase de objeto específica.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Buscar objetos por clase AD
- Active Directory, usar, buscar, por clase
- objeto AD, buscar por clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656233"
---
# <a name="finding-objects-by-class"></a>Buscar objetos por clase

Consulta de búsqueda típica para una clase de objeto específica. En el ejemplo de código siguiente se buscan equipos con ubicación en la compilación de 7N.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Tenga en cuenta por qué no se utiliza **objectClass** . No utilice **objectClass** sin otra comparación que contenga un atributo indexado. Los atributos de índice pueden aumentar la eficacia de una consulta. El atributo **objectClass** tiene varios valores y no está indizado. Para especificar el tipo o la clase de un objeto, utilice **objectCategory**.

Menos eficaz:


```C++
(objectClass=computer)
```



Más eficaz:


```C++
(objectCategory=computer)
```



Tenga en cuenta que hay algunos casos en los que se debe usar una combinación de **objectClass** y **objectCategory** . La clase de usuario y la clase de contacto deben especificarse como se indica a continuación.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



Tenga en cuenta que puede buscar usuarios y contactos con lo siguiente.


```C++
(objectCategory=person)
```



 

 




