---
title: Enumerar usuarios en servidores miembros y Windows 2000 Professional
description: En este tema se muestra cómo enumerar todos los usuarios, en una base de datos de seguridad local, en servidores miembros y equipos que se ejecutan en Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Enumeración de usuarios en servidores miembros y Windows 2000 Professional AD
- users AD, Enumerating Users on Member Servers and Windows 2000 Professional
- Active Directory, Usar, Usuarios, Enumerar usuarios en servidores miembros y Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f72e38a00e0fcc4310f7b8498b0dda28d71231df7e65fcf2de9945f5feef2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694882"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>Enumerar usuarios en servidores miembros y Windows 2000 Professional

En este tema se muestra cómo enumerar todos los usuarios, en una base de datos de seguridad local, en servidores miembros y equipos que se ejecutan en Windows 2000 Professional.

**Para enumerar los usuarios**

1.  Enlace al equipo mediante las siguientes reglas:
    1.  Use una cuenta que tenga derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace mediante el proveedor WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> , <computer> ". El parámetro " nombre de equipo " es el nombre del equipo al que &lt; se va a acceder a los &gt; grupos. Este parámetro indica a ADSI que está enlazando a un equipo y permite que el analizador del proveedor WinNT omita algunas consultas de resolución de ambigüedad para determinar a qué tipo de objeto está enlazando.
    3.  Enlace a la [**interfaz IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Agregue "user" a [**la propiedad IADsContainer.Filter.**](/windows/desktop/ADSI/iadscontainer-property-methods) Esto hace que la enumeración solo contenga objetos que tengan la clase de objeto "user".
3.  Enumerar los objetos . Para cada objeto de usuario, use los métodos de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) para leer las propiedades del usuario.

 

 