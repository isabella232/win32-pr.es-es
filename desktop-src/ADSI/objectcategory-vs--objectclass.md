---
title: objectCategory frente a objectClass
description: Los atributos objectCategory y objectClass pueden hacer referencia a una clase de esquema determinada de un objeto de directorio.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory frente a objectClass ADSI
- atributos ASI, buscar en los atributos objectCategory y objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075069"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory frente a objectClass

Los atributos **objectCategory** y **objectClass** pueden hacer referencia a una clase de esquema determinada de un objeto de directorio. Sin embargo, hay una distinción importante en la semántica entre ambos. "objectClass = Joy" hace referencia a estos objetos de directorio en los que "Joy" representa cualquier clase de la jerarquía de clases de objetos. "objectCategory = Joy", por otro lado, hace referencia a los objetos de directorio en los que "Joy" identifica una clase específica en la jerarquía de clases de objetos.

**objectClass** puede tomar varios valores, mientras que **objectCategory** toma un solo valor. Debido a esto, **objectCategory** es más adecuado para la coincidencia de tipos de objetos en una búsqueda de directorio. ADSI lo usa como criterio de coincidencia predeterminado. Las búsquedas que usan un **objectClass** no se pueden escalar a bases de datos grandes. ADSI admite las sintaxis "(objectCategory = SomeDN)" y "(objectCategory \_ = \_ nombre para mostrar de la clase LDAP \_ \_ )".

La excepción a todo esto es que el filtro de búsqueda LDAP "(objectClass = \* )" no especifica una búsqueda en la clase de objeto, sino que simplemente comprueba la presencia de los objetos.

 

 




