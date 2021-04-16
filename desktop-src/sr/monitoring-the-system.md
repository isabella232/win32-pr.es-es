---
title: Supervisando el sistema
description: Supervisando el sistema
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418321"
---
# <a name="monitoring-the-system"></a><span data-ttu-id="0e9c3-103">Supervisando el sistema</span><span class="sxs-lookup"><span data-stu-id="0e9c3-103">Monitoring the System</span></span>

<span data-ttu-id="0e9c3-104">Restaurar sistema en Windows Vista y versiones posteriores guarda una copia del volumen al generar un punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-104">System Restore in Windows Vista and later saves a copy of the volume when generating a restore point.</span></span> <span data-ttu-id="0e9c3-105">Restaurar sistema requiere un mínimo de 300 MB de espacio libre en disco en la unidad del sistema durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-105">System Restore requires a minimum of 300 MB of free disk space on the system drive at installation.</span></span>

<span data-ttu-id="0e9c3-106">Restaurar sistema en Windows XP supervisa un conjunto básico de archivos de aplicación y del sistema, y archiva los Estados de estos archivos antes de que se realicen cambios en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-106">System Restore in Windows XP monitors a core set of system and application files, archiving the states of these files before system changes are made.</span></span> <span data-ttu-id="0e9c3-107">Restaurar sistema también guarda una instantánea completa del registro y algunos archivos del sistema dinámicos.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-107">System Restore also saves a full snapshot of the registry and some dynamic system files.</span></span> <span data-ttu-id="0e9c3-108">Restaurar sistema requiere un mínimo de 200 MB de espacio libre en disco en la unidad del sistema durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-108">System Restore requires a minimum of 200 MB of free disk space on the system drive at installation.</span></span> <span data-ttu-id="0e9c3-109">Cuando la cantidad de espacio libre en disco cae por debajo de 50 MB en cualquier unidad, Restaurar sistema cambia al modo de espera y deja de crear puntos de restauración.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-109">When the amount of free disk space falls below 50 MB on any drive, System Restore switches to standby mode and stops creating restore points.</span></span> <span data-ttu-id="0e9c3-110">En ese momento se eliminan todos los puntos de restauración.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-110">All restore points are deleted at that time.</span></span> <span data-ttu-id="0e9c3-111">Restaurar sistema vuelve a activarse y reanuda la creación de puntos de restauración en cuanto 200 MB de espacio libre en disco en la unidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-111">System Restore reactivates and resumes creating restore points as soon as 200 MB of disk space is free on the system drive.</span></span> <span data-ttu-id="0e9c3-112">Los archivos que se supervisan o excluyen de la supervisión se especifican en el archivo% windir% \\ system32 \\ restore \\Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-112">The files that are monitored or excluded from monitoring are specified in the file %windir%\\system32\\restore\\Filelist.xml.</span></span> <span data-ttu-id="0e9c3-113">Para obtener más información, vea [extensiones de nombre de archivo supervisado](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0e9c3-113">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span>

 

 




