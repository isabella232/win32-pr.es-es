---
description: Al conectarse de forma remota a un servidor de Active Directory que no sea el del dominio actual, debe especificar el nombre de un equipo que ya sea miembro del dominio que pertenece al Active Directory desea.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descripción del espacio de nombres LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083136"
---
# <a name="describing-the-ldap-namespace"></a>Descripción del espacio de nombres LDAP

Al conectarse de forma remota a un servidor de Active Directory que no sea el del dominio actual, debe especificar el nombre de un equipo que ya sea miembro del dominio que pertenece al Active Directory desea.

Para conectarse de forma remota a un equipo que ya es miembro del dominio que pertenece al servidor de Active Directory, escriba el siguiente comando.

**\\\\\\Directorio raíz de equiporemoto \\ \\ LDAP**

Este ejemplo muestra que hay dos partes que componen un nombre de espacio de nombres completo. La primera parte ( \\ \\ equiporemoto) representa el equipo que ya es miembro del dominio que pertenece al servidor Active Directory que desea. La segunda parte ( \\ \\ LDAP del directorio raíz \\ ) representa el esquema de Active Directory en el proveedor de servicios de directorio.

> [!Note]  
> Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).

 

 

 



