---
title: Limpieza del directorio virtual
description: BITS extiende los directorios virtuales de IIS para admitir cargas.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995423"
---
# <a name="virtual-directory-cleanup"></a><span data-ttu-id="13d23-103">Limpieza del directorio virtual</span><span class="sxs-lookup"><span data-stu-id="13d23-103">Virtual Directory Cleanup</span></span>

<span data-ttu-id="13d23-104">BITS extiende los directorios virtuales de IIS para admitir cargas.</span><span class="sxs-lookup"><span data-stu-id="13d23-104">BITS extends IIS virtual directories to support uploads.</span></span> <span data-ttu-id="13d23-105">Cada directorio virtual tiene una propiedad de tiempo de espera de la sesión (la propiedad de la metabase [BITSSessionTimeout](bits-iis-extension-properties.md) de IIS) que especifica el período de tiempo en el que el cliente de bits debe realizar el progreso en la carga del archivo.</span><span class="sxs-lookup"><span data-stu-id="13d23-105">Each virtual directory has a session time-out property (the IIS [BITSSessionTimeout](bits-iis-extension-properties.md) metabase property) that specifies the period of time in which the BITS client must make progress in uploading the file.</span></span> <span data-ttu-id="13d23-106">Si no se realiza ningún progreso durante ese período (el temporizador se restablece cuando se realiza el progreso), BITS cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="13d23-106">If no progress is made during that period (the timer is reset when progress is made), BITS closes the session.</span></span> <span data-ttu-id="13d23-107">El tiempo de espera predeterminado de la sesión es de 14 días.</span><span class="sxs-lookup"><span data-stu-id="13d23-107">The default session time-out is 14 days.</span></span>

<span data-ttu-id="13d23-108">BITS agrega un elemento de trabajo a la [programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cada directorio virtual que se crea y se habilita.</span><span class="sxs-lookup"><span data-stu-id="13d23-108">BITS adds a work item to the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) for each virtual directory you create and enable.</span></span> <span data-ttu-id="13d23-109">El elemento de trabajo elimina los recursos asociados con las sesiones cerradas.</span><span class="sxs-lookup"><span data-stu-id="13d23-109">The work item deletes resources associated with the closed sessions.</span></span> <span data-ttu-id="13d23-110">De forma predeterminada, la limpieza se produce cada 12 horas.</span><span class="sxs-lookup"><span data-stu-id="13d23-110">By default, the cleanup occurs every 12 hours.</span></span> <span data-ttu-id="13d23-111">Si dos directorios virtuales apuntan al mismo directorio físico, el proceso de limpieza Iniciado por uno de los directorios elimina los recursos asociados a todas las sesiones cerradas en el directorio físico.</span><span class="sxs-lookup"><span data-stu-id="13d23-111">If two virtual directories point to the same physical directory, the cleanup process initiated by one of the directories deletes the resources associated with all closed sessions in the physical directory.</span></span>

<span data-ttu-id="13d23-112">Use la pestaña extensión BITS o las interfaces [programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cambiar la programación de limpieza según sea necesario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13d23-112">Use the BITS Extension tab or the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) interfaces to change the cleanup schedule as appropriate for your application.</span></span> <span data-ttu-id="13d23-113">También puede llamar al método [**IBITSExtensionSetup:: GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) para recuperar un puntero de interfaz a la tarea de limpieza asociada al directorio virtual.</span><span class="sxs-lookup"><span data-stu-id="13d23-113">You can also call the [**IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) method to retrieve an interface pointer to the cleanup task associated with the virtual directory.</span></span>

> [!Note]  
> <span data-ttu-id="13d23-114">Si el Programador de tareas está deshabilitado después de que se haya habilitado el directorio virtual, el proceso de limpieza del directorio virtual no funcionará.</span><span class="sxs-lookup"><span data-stu-id="13d23-114">If the Task Scheduler is disabled after the virtual directory is enabled, the virtual directory cleanup process will not work.</span></span>

 

 

 