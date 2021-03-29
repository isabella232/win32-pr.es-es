---
title: Agregar objetos de dominio a grupos locales
description: Los usuarios y grupos que pertenecen al dominio se pueden agregar a los grupos en el equipo local para conceder derechos al grupo o usuario de dominio en ese equipo concreto.
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, agregar objetos de dominio a grupos locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e956d1cf076f4c33c46700e52798463b7e1d2c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789646"
---
# <a name="adding-domain-objects-to-local-groups"></a>Agregar objetos de dominio a grupos locales

Cuando un servidor miembro o un equipo que se ejecuta en Windows 2000 Professional es miembro de un dominio de Windows 2000, los usuarios y grupos que pertenecen al dominio se pueden agregar a los grupos en el equipo local para conceder derechos al grupo o usuario de dominio en ese equipo concreto.

Al administrar grupos locales de dominio en un dominio de Windows 2000 mediante ADSI, se usa normalmente el proveedor LDAP. Sin embargo, al administrar grupos locales en servidores miembro y un equipo que ejecuta Windows 2000 Professional, se debe usar el proveedor de Winnt.

Solo se pueden crear grupos locales en servidores miembro y Windows 2000 Professional. Sin embargo, los grupos locales pueden contener:

-   Grupos universales y globales del bosque que contiene el dominio al que pertenece el equipo.
-   Grupos locales de dominio del dominio del equipo.
-   Usuarios de cualquier dominio del bosque.

**Para agregar un objeto de dominio a un grupo local**

1.  Enlace a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del equipo que contiene el grupo local al que se va a agregar un miembro. El enlace se debe realizar mediante una cuenta que tenga derechos suficientes para acceder a ese equipo. La cadena de enlace debe tener el formato "WinNT:// <computer name> , equipo" donde " &lt; nombre &gt; de equipo" es el nombre del grupo de equipos al que se va a agregar un miembro. El parámetro ", equipo" indica a ADSI que está enlazando a un equipo. ADSI expone estos datos al analizador del proveedor de WinNT para que pueda omitir algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando. Esto puede ahorrar al usuario una espera de 5 a 20 segundos para resolver la ambigüedad.
2.  Use el método [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) con "Group" como la clase y el nombre del grupo local como el nombre del objeto que se va a enlazar al grupo.
3.  Enlace a la interfaz [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) del grupo local al que se va a agregar un miembro.
4.  Construya el ADsPath del objeto que se va a agregar al grupo local con el formato "WinNT:// <domain> / <name> ", donde " &lt; domain &gt; " es el nombre del dominio que contiene el objeto que se va a agregar y " &lt; name &gt; " es el nombre del objeto que se va a agregar.
5.  Agregue el usuario o grupo al grupo local con el método [**IADsGroup. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) , pasando el ADsPath construido en el paso 4.

Para obtener más información y un ejemplo de código que muestra cómo agregar un objeto de usuario o grupo de dominio a un grupo local, consulte el [código de ejemplo para agregar un usuario o grupo de dominio a un grupo local](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md).

 

 