---
title: Enumerar usuarios en servidores miembro y Windows 2000 Professional
description: En este tema se muestra cómo enumerar todos los usuarios, en una base de datos de seguridad local, en servidores miembro y equipos que ejecutan Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Enumerar usuarios en servidores miembro y Windows 2000 Professional AD
- usuarios AD, enumeración de usuarios en servidores miembro y Windows 2000 Professional
- Active Directory, usar, usuarios, enumerar usuarios en servidores miembro y Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789562"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>Enumerar usuarios en servidores miembro y Windows 2000 Professional

En este tema se muestra cómo enumerar todos los usuarios, en una base de datos de seguridad local, en servidores miembro y equipos que ejecutan Windows 2000 Professional.

**Para enumerar los usuarios**

1.  Enlazar al equipo mediante las siguientes reglas:
    1.  Use una cuenta que tenga derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ". El &lt; parámetro "nombre &gt; de equipo" es el nombre del equipo para cuyos grupos tienen acceso. Este parámetro indica a ADSI que se enlaza a un equipo y permite al analizador del proveedor de WinNT omitir algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.
    3.  Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Agregue "User" a la propiedad [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) . Esto hace que la enumeración solo contenga objetos que tengan la clase de objeto "User".
3.  Enumerar los objetos. Para cada objeto de usuario, use los métodos de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) para leer las propiedades de usuario.

 

 