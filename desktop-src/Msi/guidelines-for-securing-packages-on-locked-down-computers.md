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
# <a name="securing-packages-on-locked-down-computers"></a><span data-ttu-id="b1dde-103">Protección de paquetes en equipos bloqueados</span><span class="sxs-lookup"><span data-stu-id="b1dde-103">Securing Packages on Locked-Down Computers</span></span>

<span data-ttu-id="b1dde-104">El cumplimiento de las siguientes directrices al crear un paquete de Windows Installer que se utilizará en los equipos bloqueados ayuda a mantener un entorno seguro durante la instalación:</span><span class="sxs-lookup"><span data-stu-id="b1dde-104">Adherence to the following guidelines when authoring a Windows Installer package that will be used on locked-down computers helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="b1dde-105">Pruebe el paquete para comprobar la compatibilidad con la [Directiva del sistema](system-policy.md)de Windows Installer Machine.</span><span class="sxs-lookup"><span data-stu-id="b1dde-105">Test your package for compatibility with the Windows Installer machine [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="b1dde-106">Asegúrese de que el paquete se ejecuta con todos los [niveles de interfaz de usuario](user-interface-levels.md), ninguno, básico, limitado y completo.</span><span class="sxs-lookup"><span data-stu-id="b1dde-106">Make sure you package runs with all [user interface levels](user-interface-levels.md), none, basic, limited, and full.</span></span>
-   <span data-ttu-id="b1dde-107">Pruebe el paquete en particiones NTFS, con privilegios [*elevados*](e-gly.md) y no elevados.</span><span class="sxs-lookup"><span data-stu-id="b1dde-107">Test your package on NTFS partitions, both with [*elevated*](e-gly.md) and non-elevated privileges.</span></span>
-   <span data-ttu-id="b1dde-108">A partir de Windows Installer 3,0, la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) permite a los usuarios que no son administradores revisar las aplicaciones instaladas en el contexto por equipo.</span><span class="sxs-lookup"><span data-stu-id="b1dde-108">Starting with Windows Installer 3.0, [User Account Control (UAC) Patching](user-account-control--uac--patching.md) enables non-administrator users to patch applications installed in the per-machine context.</span></span> <span data-ttu-id="b1dde-109">Pruebe el paquete de revisión en Windows Vista y Windows XP para la instalación de los usuarios con acceso de administrador y los usuarios que no sean administradores.</span><span class="sxs-lookup"><span data-stu-id="b1dde-109">Test your patch package on Windows Vista and Windows XP for both installation by users with administrator access and by non-administrator users.</span></span>

 

 



