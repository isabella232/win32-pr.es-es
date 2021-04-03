---
title: Decidir qué buscar
description: Antes de buscar en un directorio, tenga en cuenta cómo se realizará la búsqueda en función de su enfoque. Los datos y las propiedades que se van a devolver afectan al enlace para iniciar una búsqueda, la profundidad de la búsqueda, el filtro de la consulta y el rendimiento de la búsqueda.
ms.assetid: 788fa12c-9086-4d8b-bd2e-e96a494a26ad
ms.tgt_platform: multiple
keywords:
- Criterios de búsqueda Active Directory
- decidir qué buscar Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818b0f9be56830a836453c5e52ceadd52928a522
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075144"
---
# <a name="deciding-what-to-find"></a>Decidir qué buscar

Antes de buscar en un directorio, tenga en cuenta cómo se realizará la búsqueda en función de su enfoque. Los datos y las propiedades que se van a devolver afectan al enlace para iniciar una búsqueda, la profundidad de la búsqueda, el filtro de la consulta y el rendimiento de la búsqueda.

Por ejemplo, si desea buscar todos los objetos de usuario con el apellido Smith:



| Área                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dónde buscar            | Un contenedor o unidad organizativa (OU) específico dentro de un dominio, un dominio específico, un árbol de dominio específico o todo el bosque. Si busca objetos dentro de un determinado contenedor o dominio, la consulta de búsqueda funcionará mejor enlazando directamente a ese contenedor o dominio en lugar de realizar una búsqueda de subárbol en un árbol de dominios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Tipo de búsqueda             | Si comprueba la existencia de o recupera las propiedades de un objeto determinado que tiene un nombre distintivo (DN) que ya conoce, debe realizar una búsqueda base, que busca solo en el objeto al que está enlazado.<br/> Si sabe que un objeto es un descendiente directo de un contenedor determinado, enlace a ese contenedor y realice una búsqueda de un solo nivel (los objetos **attributeSchema** y **ClassSchema** en el contenedor de esquema y los objetos extendidos a la derecha en el contenedor de derechos extendidos son buenos ejemplos).<br/> Si no sabe exactamente dónde está el objeto, o si desea buscar en el objeto que ha enlazado y en todos los objetos secundarios que están por debajo en la jerarquía de directorios, realice una búsqueda de subárbol.<br/>                                                       |
| Usar índices siempre que sea posible | Por último, si busca una clase específica de objeto, el filtro de consulta debe tener expresiones que evalúen las propiedades definidas para esa clase.<br/> Para buscar objetos de grupo, incluya la expresión (objectCategory = Group) en el filtro. Para buscar objetos de usuario, especifique (& (objectClass = User) (objectCategory = person)) porque la clase de equipo se deriva de la clase de usuario, por lo que (objectClass = User) devolverá usuarios y equipos, así como los objetos de contacto y usuario tienen un **objectCategory** de Person, por lo que (objectCategory = person) devolverá los usuarios y los contactos.<br/> Para obtener más información, vea [clase de objeto y](object-class-and-object-category.md) [atributos indizados](indexed-attributes.md)y categorías de objetos.<br/> |



 

 

 





