---
title: Consulta de usuarios
description: Para consultar a un usuario, la consulta debe contener la expresión de búsqueda \ 0034;( (usuario de objectClass) (usuario objectCategory)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- usuarios AD, consulta de usuarios
- Active Directory, uso, usuarios, consulta de usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789495"
---
# <a name="querying-for-users"></a>Consulta de usuarios

Para consultar a un usuario, la consulta debe contener la expresión de búsqueda "(& (objectClass = User) (objectCategory = person))".

Dado que la clase Computer es una subclase de User, una consulta que solo contiene (objectClass = User) devolverá objetos de usuario y objetos de equipo. Además, la categoría de objeto del objeto de usuario es persona (no usuario). por lo tanto, la expresión (objectCategory = user) no devuelve ningún usuario. Si usa la expresión (objectCategory = person), la consulta devuelve objetos de usuario y objetos de contacto.

Los usuarios pueden colocarse en cualquier contenedor o unidad organizativa de un dominio, así como en la raíz del dominio. Esto significa que los usuarios pueden estar en varias ubicaciones en la jerarquía de directorios. Puede realizar una búsqueda en profundidad de "(objectCategory = user)" para buscar todos los usuarios de un contenedor, una unidad organizativa, un dominio, un árbol de dominio o un bosque, dependiendo del objeto al que esté enlazado el puntero de [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que está usando.

 

 