---
title: Agregar objetos de dominio a grupos locales
description: Los usuarios y grupos que pertenecen al dominio se pueden agregar a los grupos del equipo local para conceder derechos al usuario o grupo del dominio en ese equipo concreto.
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , agregar objetos de dominio a grupos locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fee2a90569b7a0d41db6e0654b675e7eb768ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880306"
---
# <a name="adding-domain-objects-to-local-groups"></a>Agregar objetos de dominio a grupos locales

Cuando un servidor miembro o un equipo que se ejecuta en Windows 2000 Professional es miembro de un dominio Windows 2000, los usuarios y grupos que pertenecen al dominio se pueden agregar a grupos del equipo local para conceder derechos al usuario o grupo de dominio en ese equipo concreto.

Al administrar grupos locales de dominio en Windows dominio 2000 mediante ADSI, normalmente se usa el proveedor LDAP. Sin embargo, al administrar grupos locales en servidores miembros y en un equipo Windows 2000 Professional, se debe usar el proveedor WinNT.

Solo se pueden crear grupos locales en servidores miembros y Windows 2000 Professional. Sin embargo, los grupos locales pueden contener:

-   Grupos universales y globales del bosque que contiene el dominio al que es miembro el equipo.
-   Grupos locales de dominio de ese dominio de equipo.
-   Usuarios de cualquier dominio del bosque.

**Para agregar un objeto de dominio a un grupo local**

1.  Enlace a la [**interfaz IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del equipo que contiene el grupo local al que se agregará un miembro. El enlace debe realizarse mediante una cuenta que tenga derechos suficientes para acceder a ese equipo. La cadena de enlace debe tener la forma "WinNT:// ,computer", donde " nombre de equipo " es el nombre del grupo de equipos al que se <computer name> va a agregar un &lt; &gt; miembro. El parámetro ",computer" indica a ADSI que está enlazando a un equipo. ADSI expone estos datos al analizador del proveedor winNT para que pueda omitir algunas consultas de resolución de ambigüedad para determinar a qué tipo de objeto se enlaza. Esto puede guardar al usuario una espera de 5 a 20 segundos para que se resuelva la ambigüedad.
2.  Use el [**método IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) con "group" como clase y el nombre del grupo local como nombre del objeto que se enlazará al grupo.
3.  Enlace a la [**interfaz IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) del grupo local al que se agregará un miembro.
4.  Construya el ADsPath del objeto que se va a agregar al grupo local con el formato "WinNT:// &lt; domain &gt; / &lt; &gt; name", &lt; &gt; &lt; donde " domain " &gt; es el nombre del dominio que contiene el objeto que se va a agregar y " name " es el nombre del objeto que se va a agregar.
5.  Agregue el usuario o grupo al grupo local con el método [**IADsGroup.Add,**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) pasando el ADsPath construido en el paso 4.

Para obtener más información y un ejemplo de código que muestra cómo agregar un usuario de dominio o un objeto de grupo a un grupo local, vea Ejemplo de código para agregar un usuario de dominio o un grupo [a un grupo local.](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md)

 

 
