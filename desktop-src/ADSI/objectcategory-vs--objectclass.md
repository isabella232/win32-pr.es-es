---
title: objectCategory frente a objectClass
description: Los atributos objectCategory y objectClass pueden hacer referencia a una clase de esquema determinada de un objeto de directorio.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory frente a objectClass ADSI
- atributos ASI , buscando en los atributos objectCategory y objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3833f8cf26cb2272fbe1e7c1063322f39a8c0147e4b22382d26067f90e72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839225"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory frente a objectClass

Los atributos **objectCategory y** **objectClass** pueden hacer referencia a una clase de esquema determinada de un objeto de directorio. Sin embargo, hay una diferencia importante en la semántica entre los dos. "objectClass=ijo" hace referencia a dichos objetos de directorio en los que "ala" representa cualquier clase de la jerarquía de clases de objetos. Por otro lado, "objectCategory=ijo", hace referencia a los objetos de directorio en los que "ijo" identifica una clase específica en la jerarquía de clases de objetos.

**objectClass** puede tomar varios valores, mientras **que objectCategory** toma un solo valor. Por este problema, **objectCategory** es más adecuado para la coincidencia de tipos de objetos en una búsqueda de directorios. ADSI lo usa como criterio de coincidencia predeterminado. Las búsquedas que usan **objectClass** no son escalables a bases de datos grandes. ADSI admite las sintaxis "(objectCategory=SomeDN)" y "(objectCategory=Ldap \_ Display \_ Name of \_ \_ Class)".

La excepción a todo esto es que el filtro de búsqueda LDAP "(objectClass= )" no especifica una búsqueda en la clase de objeto, sino que simplemente comprueba la presencia de \* los objetos.

 

 




