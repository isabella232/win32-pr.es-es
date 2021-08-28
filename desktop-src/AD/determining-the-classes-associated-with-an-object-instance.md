---
title: Determinar las clases asociadas a una instancia de objeto
description: Cada objeto de Active Directory Domain Services tiene dos atributos cuyos valores identifican la jerarquía de clases de objeto de las que el objeto es una instancia.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af65b5e1abf7f0bc68ae115cb409d2cdb556e08
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471501"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Determinar las clases asociadas a una instancia de objeto

Cada objeto de Active Directory Domain Services tiene dos atributos cuyos valores identifican la jerarquía de clases de objeto de las que el objeto es una instancia.




| Atributo | Descripción | 
|-----------|-------------|
| <strong>structuralObjectClass</strong> | Identifica las clases estructurales y abstractas de las que el objeto es una instancia de . Por ejemplo, los valores de un objeto de usuario pueden ser:<ul><li><strong>top</strong></li><li><strong>person</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 
| <strong>Objectclass</strong> | Identifica las clases incluidas en <strong>structuralObjectClass</strong>, además de las clases auxiliares que se adjuntan dinámicamente. Por ejemplo, si una clase auxiliar de "vehículo" está asociada a un objeto de usuario, los valores pueden ser:<ul><li><strong>top</strong></li><li><strong>Vehículo</strong></li><li><strong>person</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 




 

Tenga en cuenta que ninguno de estos atributos incluye clases auxiliares vinculadas estáticamente con las clases de objeto de las que el objeto es una instancia. Por ejemplo, la clase auxiliar **securityPrincipal**  está vinculada estáticamente a la clase de usuario porque se incluye en los valores **systemExceptionaryClass** del objeto **user classSchema;** no se incluye en los atributos **objectClass** o **structuralObjectClass** de instancias de la clase de usuario.

 

 




