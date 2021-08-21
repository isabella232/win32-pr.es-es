---
title: Consulta de usuarios
description: Para consultar a un usuario, la consulta debe contener la expresión de búsqueda \ 0034;( (objectClass user) (objectCategory person)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- usuarios de AD, consultando usuarios
- Active Directory, usar, usuarios, consultar usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae6939cef858c3dfc108611a1b0e7ab0367c302a091ca436c9c69b2fb5277b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025324"
---
# <a name="querying-for-users"></a>Consulta de usuarios

Para consultar a un usuario, la consulta debe contener la expresión de búsqueda "(&(objectClass=user)(objectCategory=person))".

Dado que la clase de equipo es una subclase de usuario, una consulta que solo contiene (objectClass=user) devolvería objetos de usuario y objetos de equipo. Además, la categoría de objeto del objeto de usuario es person (no user); por lo tanto, la expresión (objectCategory=user) no devuelve ningún usuario. Si usa la expresión (objectCategory=person), la consulta devuelve objetos de usuario y objetos de contacto.

Los usuarios se pueden colocar en cualquier contenedor o unidad organizativa de un dominio, así como en la raíz del dominio. Esto significa que los usuarios pueden estar en numerosas ubicaciones de la jerarquía de directorios. Puede realizar una búsqueda en profundidad de "(objectCategory=user)" para buscar todos los usuarios de un contenedor, una unidad organizativa, un dominio, un árbol de dominio o un bosque, en función del objeto al que esté enlazado el puntero [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que esté usando.

 

 