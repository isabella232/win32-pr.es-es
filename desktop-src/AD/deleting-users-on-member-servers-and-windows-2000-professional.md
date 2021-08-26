---
title: Eliminar usuarios en servidores miembros y Windows 2000 Professional
description: En este tema se muestra cómo eliminar un usuario de un servidor miembro o equipo que se ejecuta en Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- usuarios de AD, eliminando un usuario en servidores miembros y Windows 2000 Professional
- Active Directory, mediante, usuarios, eliminar usuarios en servidores miembros y Windows 2000 Professional
- eliminar un usuario
- servidor, eliminar un usuario
- eliminar usuarios en servidores miembros y Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e366356696c1e8b11a53b45aae3860600fc6555
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881452"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Eliminar usuarios en servidores miembros y Windows 2000 Professional

En este tema se muestra cómo eliminar un usuario de un servidor miembro o equipo que se ejecuta en Windows 2000 Professional.

**Para eliminar un usuario**

1.  Enlace al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace mediante el proveedor WinNT, el nombre del equipo y un parámetro adicional para decir a ADSI que está enlazando a un equipo: "WinNT:// <computer name> , &lt; &gt; equipo". El parámetro " &lt; nombre de equipo " es el nombre del equipo al que desea tener &gt; acceso. Este parámetro notifica a ADSI que está enlazando a un equipo y permite que el analizador del proveedor WinNT omita algunas consultas de resolución de ambigüedad para determinar a qué tipo de objeto está enlazando.
    3.  Enlace a la [**interfaz IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Especifique "user" como clase mediante [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) para eliminar el usuario.

    Tenga en cuenta que no es necesario llamar a [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar el cambio en el contenedor. La [**llamada IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma la eliminación del usuario directamente en el directorio.

 

 
