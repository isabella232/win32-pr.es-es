---
description: Para ayudar a mantener una instalación de software segura en los equipos bloqueados, siga estas instrucciones al crear el paquete de Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Protección de paquetes en equipos bloqueados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910933"
---
# <a name="securing-packages-on-locked-down-computers"></a>Protección de paquetes en equipos bloqueados

El cumplimiento de las siguientes directrices al crear un paquete de Windows Installer que se utilizará en los equipos bloqueados ayuda a mantener un entorno seguro durante la instalación:

-   Pruebe el paquete para comprobar la compatibilidad con la [Directiva del sistema](system-policy.md)de Windows Installer Machine.
-   Asegúrese de que el paquete se ejecuta con todos los [niveles de interfaz de usuario](user-interface-levels.md), ninguno, básico, limitado y completo.
-   Pruebe el paquete en particiones NTFS, con privilegios [*elevados*](e-gly.md) y no elevados.
-   A partir de Windows Installer 3,0, la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) permite a los usuarios que no son administradores revisar las aplicaciones instaladas en el contexto por equipo. Pruebe el paquete de revisión en Windows Vista y Windows XP para la instalación de los usuarios con acceso de administrador y los usuarios que no sean administradores.

 

 



