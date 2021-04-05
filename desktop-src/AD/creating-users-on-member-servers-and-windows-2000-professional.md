---
title: Creación de usuarios en servidores miembro y Windows 2000 Professional
description: En este tema se describen los pasos que se usan para crear un usuario en un servidor miembro o en un equipo que ejecuta Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Crear usuarios en servidores miembro y Windows 2000 Professional AD
- usuarios AD, creación de un usuario en servidores miembro y Windows 2000 Professional
- Active Directory, uso, usuarios, creación de un usuario en servidores miembro y Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077540"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>Creación de usuarios en servidores miembro y Windows 2000 Professional

**Para crear un usuario**

1.  Enlazar al equipo mediante las siguientes reglas:
    1.  Use una cuenta que tenga derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ". El &lt; equipo "nombre &gt; de equipo" es el nombre del equipo a cuyos grupos desea obtener acceso. Este parámetro indica a ADSI que se enlaza a un equipo y permite que el analizador del proveedor de WinNT omita algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.
    3.  Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Especifique "User" como la clase mediante [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para agregar el usuario.
3.  Escriba el usuario en la base de datos de seguridad del equipo mediante [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 