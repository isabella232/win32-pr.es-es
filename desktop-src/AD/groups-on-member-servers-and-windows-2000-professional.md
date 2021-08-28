---
title: Grupos en servidores miembros y Windows 2000 Professional
description: En servidores miembros y equipos que se ejecutan en Windows 2000 Professional, hay una base de datos de seguridad local.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Grupos en servidores miembros y Windows 2000 Professional AD
- groups AD, groups on member servers and Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e376faf96621018867e46ac021e4aeab6e7fef6cd4e304d26902cb15a4d081f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692922"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>Grupos en servidores miembros y Windows 2000 Professional

En servidores miembros y equipos que se ejecutan en Windows 2000 Professional, hay una base de datos de seguridad local. Esta base de datos de seguridad local puede contener su propio usuario local y grupos locales cuyo ámbito es solo el equipo en el que se crean. Al Windows administrar estos tipos de usuarios y grupos en servidores y equipos miembros que se ejecutan en una estación de trabajo nt o en Windows 2000 Professional, use el proveedor WinNT.

Cuando un servidor miembro o un equipo que se ejecuta en Windows 2000 Professional o Windows 2000 Professional es miembro de un dominio Windows 2000, los grupos o usuarios del dominio se pueden usar en la base de datos de seguridad local para conceder derechos a ese grupo en ese equipo determinado.

Al administrar grupos en un Windows 2000 mediante ADSI, use el proveedor LDAP. Al administrar grupos en servidores miembros y equipos que se ejecutan en Windows NT Workstation o Windows 2000 Professional, use el proveedor WinNT.

Debe enlazar, al menos una instancia, a cada proveedor: 1) Enlazar al proveedor LDAP para recuperar ADsPath al grupo o usuario que desea agregar a un grupo de la base de datos local y 2) Enlazar al proveedor de WinNT para agregar ese usuario o grupo a un grupo local.

 

 




