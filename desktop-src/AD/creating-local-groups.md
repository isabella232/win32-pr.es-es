---
title: Crear grupos locales
description: Solo se pueden crear grupos locales para los servidores miembro y Windows 2000 Professional.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Creación de grupos locales AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358808"
---
# <a name="creating-local-groups"></a>Crear grupos locales

Solo se pueden crear grupos locales para los servidores miembro y Windows 2000 Professional.

**Para crear un grupo local para un servidor miembro o un equipo que ejecute Windows 2000 Professional**

1.  Enlazar al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para tener acceso a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ".

        El &lt; parámetro "nombre &gt; de equipo" es el nombre de los grupos de equipos a los que se va a obtener acceso.

        En la cadena de enlace, el &lt; parámetro "equipo &gt; " indica a ADSI que está enlazando a un equipo. ADSI hace que estos datos estén disponibles para el analizador del proveedor de WinNT, de modo que pueda omitir algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.

    3.  Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Especifique "localGroup" como clase mediante [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para agregar el grupo.
    > [!Note]  
    > Si especifica "Group" como la clase, ADSI utiliza "localGroup". No especifique la clase como "globalGroup". No se pueden crear grupos de la clase "globalGroup" en los servidores miembro o en un equipo que ejecute Windows NT Workstation/Windows 2000 Professional. Si especifica "globalGroup", [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crea el grupo en la caché de propiedades, pero [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) no escribe el grupo en la base de datos de seguridad y no devuelve un error.

     

3.  Escriba el grupo en la base de datos de seguridad del equipo mediante [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 