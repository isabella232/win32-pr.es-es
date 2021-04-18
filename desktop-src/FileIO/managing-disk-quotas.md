---
description: Los administradores pueden controlar la cantidad de datos que cada usuario puede almacenar en un volumen del sistema de archivos NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Administración de cuotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688456"
---
# <a name="managing-disk-quotas"></a><span data-ttu-id="5c32f-103">Administración de cuotas de disco</span><span class="sxs-lookup"><span data-stu-id="5c32f-103">Managing Disk Quotas</span></span>

<span data-ttu-id="5c32f-104">El sistema de archivos NTFS admite *cuotas de disco*, lo que permite a los administradores controlar la cantidad de datos que cada usuario puede almacenar en un volumen del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="5c32f-104">The NTFS file system supports *disk quotas*, which allow administrators to control the amount of data that each user can store on an NTFS file system volume.</span></span> <span data-ttu-id="5c32f-105">Los administradores pueden configurar opcionalmente el sistema para registrar un evento cuando los usuarios están cerca de su cuota y para denegar más espacio en disco a los usuarios que superan su cuota.</span><span class="sxs-lookup"><span data-stu-id="5c32f-105">Administrators can optionally configure the system to log an event when users are near their quota, and to deny further disk space to users who exceed their quota.</span></span> <span data-ttu-id="5c32f-106">Los administradores también pueden generar informes y usar el monitor de eventos para realizar el seguimiento de los problemas de cuota.</span><span class="sxs-lookup"><span data-stu-id="5c32f-106">Administrators can also generate reports, and use the event monitor to track quota issues.</span></span>

<span data-ttu-id="5c32f-107">Puede determinar si un sistema de archivos admite cuotas de disco llamando a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examinando la marca de bits de **\_ \_ cuotas de volumen de archivo** .</span><span class="sxs-lookup"><span data-stu-id="5c32f-107">You can determine whether a file system supports disk quotas by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_VOLUME\_QUOTAS** bit flag.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5c32f-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5c32f-108">In this section</span></span>



| <span data-ttu-id="5c32f-109">Tema</span><span class="sxs-lookup"><span data-stu-id="5c32f-109">Topic</span></span>                                                                                                   | <span data-ttu-id="5c32f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c32f-110">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c32f-111">Administración de las cuotas de disco en el nivel de usuario</span><span class="sxs-lookup"><span data-stu-id="5c32f-111">User-level Administration of Disk Quotas</span></span>](user-level-administration-of-disk-quotas.md)<br/>     | <span data-ttu-id="5c32f-112">Cómo obtener más espacio libre en disco después de superar la asignación de cuota.</span><span class="sxs-lookup"><span data-stu-id="5c32f-112">How to get more free disk space after exceeding the quota allowance.</span></span><br/>                                                                  |
| [<span data-ttu-id="5c32f-113">Administración de las cuotas de disco en el nivel de sistema</span><span class="sxs-lookup"><span data-stu-id="5c32f-113">System-level Administration of Disk Quotas</span></span>](system-level-administration-of-disk-quotas.md)<br/> | <span data-ttu-id="5c32f-114">El administrador del sistema puede establecer cuotas para usuarios específicos en un volumen.</span><span class="sxs-lookup"><span data-stu-id="5c32f-114">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="5c32f-115">Además, el administrador puede establecer cuotas predeterminadas para el volumen.</span><span class="sxs-lookup"><span data-stu-id="5c32f-115">The administrator can also set default quotas for the volume.</span></span><br/> |
| [<span data-ttu-id="5c32f-116">Límites de cuota de disco</span><span class="sxs-lookup"><span data-stu-id="5c32f-116">Disk Quota Limits</span></span>](disk-quota-limits.md)<br/>                                                   | <span data-ttu-id="5c32f-117">Describe dos tipos de límites de cuota de disco y cómo se miden los límites de cuota de disco.</span><span class="sxs-lookup"><span data-stu-id="5c32f-117">Describes two types of disk quota limits and how disk quota limits are measured.</span></span><br/>                                                      |
| [<span data-ttu-id="5c32f-118">Interfaces de cuota de disco</span><span class="sxs-lookup"><span data-stu-id="5c32f-118">Disk Quota Interfaces</span></span>](disk-quota-interfaces.md)<br/>                                           | <span data-ttu-id="5c32f-119">Interfaces utilizadas con cuotas de disco.</span><span class="sxs-lookup"><span data-stu-id="5c32f-119">Interfaces used with disk quotas.</span></span><br/>                                                                                                     |



 

 

 




