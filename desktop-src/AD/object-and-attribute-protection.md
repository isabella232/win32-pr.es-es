---
title: Protección de objetos y atributos
description: Una lista de control de acceso (ACL) protege todos los objetos de Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Protección de objetos y atributos
- seguridad AD, protección de objetos y atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773129"
---
# <a name="object-and-attribute-protection"></a>Protección de objetos y atributos

Una lista de control de acceso (ACL) protege todos los objetos de Active Directory Domain Services. Las ACL determinan quién puede ver el objeto, qué atributos pueden leer y las acciones que cada usuario puede realizar en el objeto. La existencia de un objeto o un atributo no se revela nunca a un usuario no autorizado.

Una ACL es una lista de entradas de control de acceso (ACE) almacenadas con el objeto que protege. En Windows NT y Windows 2000, las ACL se almacenan como valores binarios, denominados descriptores de seguridad. Cada ACE contiene un identificador de seguridad (SID), que identifica la entidad de seguridad (usuario o grupo) a la que se aplica la ACE y los datos sobre el tipo de acceso que la ACE concede o deniega.

Las ACL de los objetos de directorio contienen ACE que se aplican al objeto como un todo y las ACE que se aplican a los atributos individuales del objeto. Esto permite a un administrador controlar no solo qué usuarios pueden ver un objeto, sino también qué propiedades pueden ver los usuarios. Por ejemplo, a todos los usuarios se les puede conceder acceso de lectura a los atributos de número de teléfono y correo electrónico para todos los demás usuarios, pero las propiedades de seguridad de los usuarios pueden denegarse a todos los miembros de un grupo de administradores de seguridad especial. A los usuarios individuales se les puede conceder acceso de escritura a los atributos personales, como las direcciones de teléfono y correo electrónico de sus propios objetos de usuario.

 

 




