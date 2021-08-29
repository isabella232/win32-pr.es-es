---
title: Nombres de objeto e identidades
description: Un objeto de Active Directory Domain Services tiene varias identidades, incluidas las siguientes.
ms.assetid: ad8bc74d-45a8-4df3-bfb8-35dd376b9c0b
ms.tgt_platform: multiple
keywords:
- nombres de objeto e identidades Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dc3e79cd40eebb47fe85b14f50130750cdb4a1cea884d8ebf50a89555d2ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025592"
---
# <a name="object-names-and-identities"></a>Nombres de objeto e identidades

Un objeto de Active Directory Domain Services tiene varias identidades, incluidas las siguientes.

## <a name="relative-distinguished-name"></a>Nombre distintivo relativo

El nombre distintivo relativo es el nombre definido por el atributo de nomenclatura de un objeto. El **atributo rDnAttID de** un objeto **classSchema** identifica el atributo de nomenclatura para las instancias de la clase . La mayoría de las clases de **objeto usan** el atributo cn (Common-Name) como atributo de nomenclatura. El nombre distintivo relativo de un objeto debe ser único en el contenedor donde reside el objeto. Puede haber muchas instancias de objeto con el mismo nombre distintivo relativo, pero no dos pueden estar en el mismo contenedor. Para obtener más información sobre el **atributo rDnAttID** y los objetos **classSchema,** vea [Características de las clases de objeto](characteristics-of-object-classes.md).

## <a name="distinguished-name"></a>Nombre completo

El [*nombre distintivo es*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) el nombre actual del objeto y se encuentra en el atributo **distinguishedName** del objeto. El nombre distintivo es una cadena que incluye la ubicación del objeto y se forma concatenando el nombre distintivo relativo del objeto y cada uno de sus antecesores hasta la raíz. Por ejemplo, el nombre distintivo del contenedor Users del dominio Fabrikam.com sería "CN=Users,DC=Fabrikam,DC=com". Los nombres distintivos son únicos dentro de un bosque. El nombre distintivo de un objeto cambia cuando se mueve o se cambia el nombre del objeto.

## <a name="object-guid"></a>GUID de objeto

El GUID del objeto es un identificador único global asignado por Active Directory Domain Services cuando se crea la instancia de objeto. El GUID del objeto se encuentra en el **atributo objectGUID** del objeto. Un GUID es un número de 128 bits que se garantiza que es único en espacio y tiempo. Los GUID de objeto nunca cambian, por lo que si se cambia el nombre de un objeto o se mueve a cualquier parte del bosque empresarial, el GUID del objeto sigue siendo el mismo. Las aplicaciones que guarden referencias a objetos en Active Directory Domain Services deben usar el GUID del objeto para asegurarse de que la referencia de objeto sobrevivirá a un cambio de nombre del objeto. El nombre distintivo de un objeto puede cambiar, pero el GUID del objeto no lo hará.

## <a name="other-identities"></a>Otras identidades

Las instancias de objeto pueden tener muchos otros atributos y los atributos se pueden usar para la identificación por parte de las aplicaciones. Por ejemplo, los objetos de entidad de seguridad  (instancias de las clases de usuario **,** equipo y objeto de grupo) tienen los atributos **userPrincipalName**, **sAMAccountName** y **objectSid.** Estos atributos son "nombres" muy importantes para Windows 2000, pero no forman parte de la identidad del objeto desde la perspectiva del directorio.

 

 