---
title: Eliminación de usuarios en servidores miembro y Windows 2000 Professional
description: En este tema se muestra cómo eliminar un usuario de un servidor miembro o un equipo que ejecuta en Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- usuarios AD, eliminación de un usuario en servidores miembro y Windows 2000 Professional
- Active Directory, uso, usuarios, eliminación de usuarios en servidores miembro y Windows 2000 Professional
- eliminación de un usuario
- servidor, eliminación de un usuario
- eliminación de usuarios en servidores miembro y Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077532"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Eliminación de usuarios en servidores miembro y Windows 2000 Professional

En este tema se muestra cómo eliminar un usuario de un servidor miembro o un equipo que ejecuta en Windows 2000 Professional.

**Para eliminar un usuario**

1.  Enlazar al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para tener acceso a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ". El &lt; parámetro "nombre &gt; de equipo" es el nombre del equipo a cuyos grupos desea obtener acceso. Este parámetro notifica a ADSI que está enlazando a un equipo y permite al analizador del proveedor de WinNT omitir algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.
    3.  Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Especifique "User" como la clase mediante [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) para eliminar el usuario.

    Tenga en cuenta que no es necesario llamar a [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar el cambio en el contenedor. La llamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma la eliminación del usuario directamente en el directorio.

 

 