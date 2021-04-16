---
description: Restaurar sistema supervisa y registra automáticamente los cambios del sistema de claves en el equipo de un usuario. Para obtener más información, consulte Restaurar sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Puntos de restauración del sistema y el Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677526"
---
# <a name="system-restore-points-and-the-windows-installer"></a><span data-ttu-id="843a6-104">Puntos de restauración del sistema y el Windows Installer</span><span class="sxs-lookup"><span data-stu-id="843a6-104">System Restore Points and the Windows Installer</span></span>

<span data-ttu-id="843a6-105">Restaurar sistema supervisa y registra automáticamente los cambios del sistema de claves en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="843a6-105">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="843a6-106">Para obtener más información, consulte [Restaurar sistema](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="843a6-106">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="843a6-107">Los puntos de restauración del sistema los crea el sistema y también los crea Windows Installer cuando se instala o se quita software.</span><span class="sxs-lookup"><span data-stu-id="843a6-107">System restore points are created by the system and are also created by Windows Installer when software is installed or removed.</span></span>

<span data-ttu-id="843a6-108">En Windows XP, el instalador puede crear puntos de control durante la primera instalación de una aplicación y durante su eliminación.</span><span class="sxs-lookup"><span data-stu-id="843a6-108">On Windows XP, the installer may create checkpoints during the first installation of an application, and during its removal.</span></span> <span data-ttu-id="843a6-109">El instalador solo crea puntos de control en estos casos cuando el cambio se ejecuta con al menos una [*interfaz de usuario básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="843a6-109">The installer only creates checkpoints in these cases when the change is run with at least a [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="843a6-110">Las instalaciones que tienen el [nivel de interfaz de usuario](user-interface-levels.md) establecido en None normalmente las inicia el sistema o una aplicación que debe administrar la creación de un punto de control.</span><span class="sxs-lookup"><span data-stu-id="843a6-110">Installations having the [user interface level](user-interface-levels.md) set to None are usually initiated by the system or an application that should handle creating a checkpoint.</span></span> <span data-ttu-id="843a6-111">Para obtener más información, consulte [Restaurar sistema](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="843a6-111">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="843a6-112">En organizaciones con muchas aplicaciones pequeñas, los administradores pueden decidir deshabilitar los puntos de comprobación desde el instalador para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="843a6-112">In corporations with many small applications, administrators may decide to disable checkpointing from within the installer to improve performance.</span></span> <span data-ttu-id="843a6-113">Para obtener más información, vea [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) o [establecer un punto de restauración desde una acción personalizada](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="843a6-113">For more information, see [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) or [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

<span data-ttu-id="843a6-114">A partir de Windows Installer 5,0, la propiedad [**MSIFASTINSTALL**](msifastinstall.md) se puede establecer para impedir que una instalación genere un punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="843a6-114">Beginning with Windows Installer 5.0, the [**MSIFASTINSTALL**](msifastinstall.md) property can be set to prevent an installation from generating a system restore point.</span></span>

 

 
