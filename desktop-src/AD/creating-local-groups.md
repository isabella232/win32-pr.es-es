---
title: Creación de grupos locales
description: Solo se pueden crear grupos locales para servidores miembros y Windows 2000 Professional.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Creación de grupos locales de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06410572e6e5897280b2a03c99b387dbf81b3cca
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881588"
---
# <a name="creating-local-groups"></a>Creación de grupos locales

Solo se pueden crear grupos locales para servidores miembros y Windows 2000 Professional.

**Para crear un grupo local para un servidor miembro o equipo que ejecute Windows 2000 Professional**

1.  Enlace al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor winNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> , &lt; &gt; equipo".

        El parámetro " &lt; nombre de equipo " es el nombre de los grupos de equipos a los que se va a &gt; acceder.

        En la cadena de enlace, el parámetro " equipo " indica &lt; &gt; a ADSI que está enlazando a un equipo. ADSI pone estos datos a disposición del analizador del proveedor winNT para que pueda omitir algunas consultas de resolución de ambigüedad para determinar a qué tipo de objeto se enlaza.

    3.  Enlace a la [**interfaz IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Especifique "localGroup" como clase mediante [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para agregar el grupo.
    > [!Note]  
    > Si especifica "group" como clase, ADSI usa "localGroup". No especifique la clase como "globalGroup". No se pueden crear grupos de clase "globalGroup" en servidores miembros o en un equipo que ejecute Windows NT Workstation/Windows 2000 Professional. Si especifica "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crea el grupo en la caché de propiedades, pero [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) no escribe el grupo en la base de datos de seguridad y no devuelve un error.

     

3.  Escriba el grupo en la base de datos de seguridad del equipo [**mediante IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 
