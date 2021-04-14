---
description: El escritor de Active Directory no requiere ninguna acción especial durante las operaciones de copia de seguridad.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Copia de seguridad y restauración de VSS del Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541747"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a><span data-ttu-id="22228-103">Copia de seguridad y restauración de VSS del Active Directory</span><span class="sxs-lookup"><span data-stu-id="22228-103">VSS Backup and Restore of the Active Directory</span></span>

<span data-ttu-id="22228-104">El escritor de Active Directory no requiere ninguna acción especial durante las operaciones de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="22228-104">The Active Directory writer requires no special actions during backup operations.</span></span> <span data-ttu-id="22228-105">El escritor proporcionará al solicitante la información del componente y del conjunto de archivos, y el solicitante usará esa información para decidir qué archivos copiar en el medio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="22228-105">The writer will provide the requester with component and file set information, and the requester uses that information to decide which files to copy to backup media.</span></span> <span data-ttu-id="22228-106">No es necesario usar ninguna API especial para realizar una copia de seguridad del Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22228-106">There is no need to use any special APIs to back up the Active Directory.</span></span>

<span data-ttu-id="22228-107">La forma en que se realice una restauración dependerá de si el Active Directory se restaura como parte de una operación de recuperación ante desastres o de si la restauración se realiza en un sistema en el que se ejecuta la Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22228-107">How a restore is performed depends on whether the Active Directory is be restored as part of a disaster recovery operation, or if the restore is to a system on which the Active Directory is running.</span></span> <span data-ttu-id="22228-108">Además, la antigüedad de la copia de seguridad del estado Active Directory puede ser un problema debido a Active Directory marcadores de exclusión.</span><span class="sxs-lookup"><span data-stu-id="22228-108">In addition, the age of the backup copy of the Active Directory state may be an issue because of Active Directory tombstones.</span></span>

## <a name="active-directory-restoration-following-disaster-recovery"></a><span data-ttu-id="22228-109">Active Directory restauración después de la recuperación ante desastres</span><span class="sxs-lookup"><span data-stu-id="22228-109">Active Directory Restoration following Disaster Recovery</span></span>

<span data-ttu-id="22228-110">Tras un bloqueo que requiere recuperación ante desastres, el Active Directory se puede restaurar como parte de la restauración del estado del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="22228-110">Following a crash requiring disaster recovery, the Active Directory can be restored as part of the restoration of the operating system state.</span></span>

<span data-ttu-id="22228-111">Esta operación de restauración es esencialmente una restauración sin escritor.</span><span class="sxs-lookup"><span data-stu-id="22228-111">This restore operation is essentially a writerless restore.</span></span>

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a><span data-ttu-id="22228-112">Active Directory restauración en el sistema donde se está ejecutando</span><span class="sxs-lookup"><span data-stu-id="22228-112">Active Directory Restoration on the System where It Is Running</span></span>

<span data-ttu-id="22228-113">El sistema debe reiniciarse en el modo de restauración de servicios de directorio si el Active Directory se está ejecutando actualmente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="22228-113">The system must be rebooted in Directory Services Restore mode if the Active Directory is currently running on the server.</span></span>

<span data-ttu-id="22228-114">Después, el sistema operativo se ejecutará sin el Active Directory y toda la validación del usuario se realizará a través del administrador de cuentas de seguridad (SAM) en el registro.</span><span class="sxs-lookup"><span data-stu-id="22228-114">The operating system will then be running without the Active Directory, and all user validation occurs through the Security Accounts Manager (SAM) in the registry.</span></span> <span data-ttu-id="22228-115">Solo el administrador tiene permiso para recuperar el Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22228-115">Only the administrator has permission to recover the Active Directory.</span></span>

<span data-ttu-id="22228-116">Una vez en el modo de restauración del servicio de directorio, una restauración de VSS puede continuar con normalidad.</span><span class="sxs-lookup"><span data-stu-id="22228-116">Once in Directory Service Restore mode, a VSS restore can proceed normally.</span></span> <span data-ttu-id="22228-117">No hay ninguna razón para usar las API de Active Directory de Win32 que no son de VSS para restaurar el estado de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22228-117">There is no reason to use non-VSS Win32 Active Directory APIs to restore the Active Directory state.</span></span>

## <a name="active-directory-restores-and-active-directory-tombstones"></a><span data-ttu-id="22228-118">Active Directory restaura y Active Directory marcadores de exclusión</span><span class="sxs-lookup"><span data-stu-id="22228-118">Active Directory Restores and Active Directory Tombstones</span></span>

<span data-ttu-id="22228-119">Cualquier plan de recuperación debe asegurarse de que la antigüedad de la copia de seguridad no debe superar la duración del desecho Active Directory (el valor predeterminado es 60 días).</span><span class="sxs-lookup"><span data-stu-id="22228-119">Any recovery plan should ensure that the age of the backup should not exceed the Active Directory Tombstone Lifetime (default is 60 days).</span></span>

<span data-ttu-id="22228-120">La restauración de una copia de seguridad anterior al objeto de desecho hará que un controlador de dominio tenga objetos que no se repliquen en los otros servidores.</span><span class="sxs-lookup"><span data-stu-id="22228-120">Restoration of a backup older than the tombstone will cause a domain controller to have objects that are not replicated to the other servers.</span></span>

<span data-ttu-id="22228-121">Los objetos que no se replican no se eliminarán automáticamente en el controlador de dominio (restaurado), ya que los marcadores de exclusión de esos objetos en las otras réplicas ya se han eliminado.</span><span class="sxs-lookup"><span data-stu-id="22228-121">Those objects that are not replicated will not be deleted automatically on that (restored) domain controller because the tombstones of those objects on the other replicas have already been deleted.</span></span>

<span data-ttu-id="22228-122">Un administrador tendrá que eliminar manualmente cada uno de los objetos del controlador de dominio restaurado que no se repliquen.</span><span class="sxs-lookup"><span data-stu-id="22228-122">An administrator will have to manually delete each of the objects on the restored domain controller that are not replicated.</span></span> <span data-ttu-id="22228-123">No se admiten copias de seguridad incrementales del Active Directory; se requiere una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="22228-123">Incremental backups of the Active Directory are not supported; a full backup is required.</span></span>

 

 



