---
description: Para ayudar a mantener una instalación segura de software en equipos bloqueados, siga estas instrucciones al crear el paquete Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Protección de paquetes en equipos bloqueados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bcdb2770e165a8b0d99fbc2088ec4c3b113e5befa180a7d6d2598eee866a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315305"
---
# <a name="securing-packages-on-locked-down-computers"></a>Protección de paquetes en equipos bloqueados

El cumplimiento de las siguientes directrices al crear un paquete Windows Installer que se usará en equipos bloqueados ayuda a mantener un entorno seguro durante la instalación:

-   Pruebe la compatibilidad del paquete con la directiva de sistema del Windows del [instalador.](system-policy.md)
-   Asegúrese de que el paquete se ejecuta con todos los [niveles de interfaz de usuario](user-interface-levels.md), ninguno, básico, limitado y lleno.
-   Pruebe el paquete en particiones NTFS, tanto con [*privilegios*](e-gly.md) elevados como sin privilegios elevados.
-   A partir de Windows Installer 3.0, la aplicación de revisiones de control de cuentas de usuario [(UAC)](user-account-control--uac--patching.md) permite a los usuarios que no son administradores aplicar revisiones a las aplicaciones instaladas en el contexto por equipo. Pruebe el paquete de revisión en Windows Vista y Windows XP para la instalación tanto de usuarios con acceso de administrador como de usuarios que no son administradores.

 

 



