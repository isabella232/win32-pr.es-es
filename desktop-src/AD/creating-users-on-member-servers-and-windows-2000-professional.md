---
title: Creación de usuarios en servidores miembros y Windows 2000 Professional
description: En este tema se describen los pasos que se usan para crear un usuario en un servidor miembro o equipo que ejecuta Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Creación de usuarios en servidores miembros y Windows 2000 Professional AD
- users AD , creando un usuario en servidores miembros y Windows 2000 Professional
- Active Directory, usar, usuarios, crear un usuario en servidores miembros y Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21490302b025e20f836cbbc957d0f86824b3456d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881578"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>Creación de usuarios en servidores miembros y Windows 2000 Professional

**Para crear un usuario**

1.  Enlace al equipo mediante las siguientes reglas:
    1.  Use una cuenta que tenga derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor winNT, el nombre del equipo y un parámetro adicional para decir a ADSI que está enlazando a un equipo: "WinNT:// <computer name> , &lt; &gt; equipo". El equipo "nombre de equipo" es el nombre del equipo al que &lt; &gt; desea acceder. Este parámetro indica a ADSI que está enlazando a un equipo y permite que el analizador del proveedor winNT omita algunas consultas de resolución de ambigüedad para determinar a qué tipo de objeto está enlazando.
    3.  Enlace a la [**interfaz IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Especifique "user" como clase mediante [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para agregar el usuario.
3.  Escriba el usuario en la base de datos de seguridad del equipo [**mediante IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 
