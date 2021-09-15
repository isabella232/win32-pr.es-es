---
description: Al conectarse de forma remota a un servidor Active Directory distinto del del dominio actual, debe especificar el nombre de un equipo que ya sea miembro del dominio que pertenece al Active Directory que desee.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descripción del espacio de nombres LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575365"
---
# <a name="describing-the-ldap-namespace"></a>Descripción del espacio de nombres LDAP

Al conectarse de forma remota a un servidor Active Directory distinto del del dominio actual, debe especificar el nombre de un equipo que ya sea miembro del dominio que pertenece al Active Directory que desee.

Para conectarse de forma remota a un equipo que ya sea miembro del dominio que pertenece al servidor Active Directory, escriba el siguiente comando.

**\\\\LDAP del directorio raíz de RemoteComputer \\ \\ \\**

En este ejemplo se muestra que hay dos partes que son un nombre de espacio de nombres completo. La primera parte \\ (RemoteComputer) representa el equipo que ya es miembro del dominio que pertenece al Active Directory \\ servidor que desea. La segunda parte \\ \\ (LDAP del \\ directorio raíz) representa el esquema Active Directory en el proveedor de servicios de directorio.

> [!Note]  
> Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del [sistema operativo de componentes WMI](operating-system-availability-of-wmi-components.md).

 

 

 



