---
title: Nombres e identidades de objeto
description: Un objeto de Active Directory Domain Services tiene varias identidades, entre las que se incluyen las siguientes.
ms.assetid: ad8bc74d-45a8-4df3-bfb8-35dd376b9c0b
ms.tgt_platform: multiple
keywords:
- nombres e identidades de objeto Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a803b4cc068a3ee0f9e2a75f61ff239c1d971bf3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487419"
---
# <a name="object-names-and-identities"></a>Nombres e identidades de objeto

Un objeto de Active Directory Domain Services tiene varias identidades, entre las que se incluyen las siguientes.

## <a name="relative-distinguished-name"></a>Nombre distintivo relativo

El nombre distintivo relativo es el nombre definido por el atributo de nomenclatura de un objeto. El atributo **rDnAttID** de un objeto **ClassSchema** identifica el atributo de nomenclatura para las instancias de la clase. La mayoría de las clases de objeto usan el atributo **CN** (Common-Name) como atributo de nomenclatura. El nombre distintivo relativo de un objeto debe ser único en el contenedor donde reside el objeto. Puede haber muchas instancias de objeto con el mismo nombre distintivo relativo, pero dos no pueden estar en el mismo contenedor. Para obtener más información sobre el atributo **rDnAttID** y los objetos **ClassSchema** , vea [características de las clases de objeto](characteristics-of-object-classes.md).

## <a name="distinguished-name"></a>Nombre completo

El [*nombre distintivo*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) es el nombre actual del objeto y se encuentra en el atributo **distinguishedName** del objeto. El nombre distintivo es una cadena que incluye la ubicación del objeto y se forma concatenando el nombre distintivo relativo del objeto y cada uno de sus antecesores hasta la raíz. Por ejemplo, el nombre distintivo del contenedor de usuarios en el dominio Fabrikam.com sería "CN = users, DC = Fabrikam, DC = com". Los nombres distintivos son únicos dentro de un bosque. El nombre distintivo de un objeto cambia cuando el objeto se mueve o se cambia de nombre.

## <a name="object-guid"></a>GUID del objeto

El GUID del objeto es un identificador único global asignado por Active Directory Domain Services cuando se crea la instancia del objeto. El GUID del objeto se encuentra en el atributo **objectGUID** del objeto. Un GUID es un número de 128 bits garantizado que es único en el espacio y en el tiempo. Los GUID de objeto nunca cambian, por lo que si se cambia el nombre de un objeto o se mueve en cualquier parte del bosque de la empresa, el GUID del objeto sigue siendo el mismo. Las aplicaciones que guardan referencias a objetos de Active Directory Domain Services deben usar el GUID del objeto para asegurarse de que la referencia al objeto sobreviverá a un cambio de nombre del objeto. El nombre distintivo de un objeto puede cambiar, pero el GUID del objeto no lo hará.

## <a name="other-identities"></a>Otras identidades

Las instancias de objeto pueden tener muchos otros atributos, y los atributos se pueden usar para la identificación de las aplicaciones. Por ejemplo, los objetos de entidad de seguridad (instancias de las clases de objetos de **usuario**, **equipo** y **Grupo** ) tienen los atributos **userPrincipalName**, **samAccountName** y **objectSid** . Estos atributos son muy importantes "Names" para Windows 2000, pero no forman parte de la identidad del objeto desde la perspectiva del directorio.

 

 