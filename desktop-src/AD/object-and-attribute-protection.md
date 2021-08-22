---
title: Protección de objetos y atributos
description: Una lista de control de acceso (ACL) protege todos los objetos de Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Protección de objetos y atributos
- security AD, protección de objetos y atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7798ca1498c3a8ffe58bf43117dfd8ae249d234115f551c636628ad5b811e04a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025624"
---
# <a name="object-and-attribute-protection"></a>Protección de objetos y atributos

Una lista de control de acceso (ACL) protege todos los objetos de Active Directory Domain Services. Las ACL determinan quién puede ver el objeto, qué atributos puede leer y qué acciones puede realizar cada usuario en el objeto. La existencia de un objeto o un atributo nunca se revela a un usuario no autorizado.

Una ACL es una lista de entradas de control de acceso (ACE) almacenadas con el objeto que protege. En Windows NT y Windows 2000, una ACL se almacena como un valor binario, denominado descriptor de seguridad. Cada ACE contiene un identificador de seguridad (SID), que identifica la entidad de seguridad (usuario o grupo) a la que se aplica la ACE y los datos sobre qué tipo de acceso concede o deniega la ACE.

Las ACL de los objetos de directorio contienen ACE que se aplican al objeto en su conjunto y LAS ACL que se aplican a los atributos individuales del objeto. Esto permite a un administrador controlar no solo qué usuarios pueden ver un objeto, sino también qué propiedades pueden ver esos usuarios. Por ejemplo, a todos los usuarios se les podría conceder acceso de lectura a los atributos de correo electrónico y número de teléfono para todos los demás usuarios, pero es posible que se denieguen las propiedades de seguridad de los usuarios a todos los miembros menos a los miembros de un grupo especial de administradores de seguridad. A los usuarios individuales se les podría conceder acceso de escritura a atributos personales, como el teléfono y las direcciones de correo electrónico en sus propios objetos de usuario.

 

 




