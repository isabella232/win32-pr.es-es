---
description: Al conectarse de forma remota a un servidor Active Directory distinto del del dominio actual, debe especificar el nombre de un equipo que ya sea miembro del dominio que pertenece al Active Directory que desea.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descripción del espacio de nombres LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad19ea98e5bd6f36ff78159bfe0a106f0772921c152aa167c38e435732188446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568625"
---
# <a name="describing-the-ldap-namespace"></a>Descripción del espacio de nombres LDAP

Al conectarse de forma remota a un servidor Active Directory distinto del del dominio actual, debe especificar el nombre de un equipo que ya sea miembro del dominio que pertenece al Active Directory que desea.

Para conectarse de forma remota a un equipo que ya sea miembro del dominio que pertenece al servidor Active Directory, escriba el siguiente comando.

**\\\\LDAP del directorio raíz de RemoteComputer \\ \\ \\**

En este ejemplo se muestra que hay dos partes que son un nombre de espacio de nombres completo. La primera parte \\ (RemoteComputer) representa el equipo que ya es miembro del dominio que pertenece al Active Directory \\ servidor que desea. La segunda parte \\ \\ (LDAP del directorio raíz) representa el esquema Active Directory en el \\ proveedor de servicios de directorio.

> [!Note]  
> Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del sistema operativo [de componentes WMI](operating-system-availability-of-wmi-components.md).

 

 

 



