---
description: Describe dos tipos de límites de cuota de disco y cómo se miden los límites de cuota de disco.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Límites de cuota de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667700"
---
# <a name="disk-quota-limits"></a><span data-ttu-id="03938-103">Límites de cuota de disco</span><span class="sxs-lookup"><span data-stu-id="03938-103">Disk Quota Limits</span></span>

<span data-ttu-id="03938-104">El espacio en disco que utiliza cada archivo se cobra directamente al usuario que posee el archivo.</span><span class="sxs-lookup"><span data-stu-id="03938-104">The disk space that each file uses is charged directly to the user who owns the file.</span></span> <span data-ttu-id="03938-105">El propietario de un archivo se identifica mediante el identificador de seguridad (SID) en la información de seguridad del archivo.</span><span class="sxs-lookup"><span data-stu-id="03938-105">The owner of a file is identified by the security identifier (SID) in the security information for the file.</span></span> <span data-ttu-id="03938-106">El espacio total en disco que se carga a un usuario es la suma de la longitud de todos los flujos de datos.</span><span class="sxs-lookup"><span data-stu-id="03938-106">The total disk space charged to a user is the sum of the length of all data streams.</span></span> <span data-ttu-id="03938-107">En otras palabras, los flujos de conjuntos de propiedades y los flujos de datos de usuario residentes afectan a la cuota del usuario.</span><span class="sxs-lookup"><span data-stu-id="03938-107">In other words, property set streams and resident user data streams affect the user's quota.</span></span>

<span data-ttu-id="03938-108">La cuota no se cobra por puntos de reanálisis, descriptores de seguridad u otros metadatos asociados a los archivos.</span><span class="sxs-lookup"><span data-stu-id="03938-108">Quota is not charged for re-parse points, security descriptors, or other metadata that is associated with the files.</span></span> <span data-ttu-id="03938-109">La compresión o descompresión de archivos no afecta al espacio en disco indicado para los archivos.</span><span class="sxs-lookup"><span data-stu-id="03938-109">Compressing or decompressing files does not affect the disk space reported for the files.</span></span> <span data-ttu-id="03938-110">Por lo tanto, la configuración de cuota de un volumen puede compararse con la configuración de otro volumen.</span><span class="sxs-lookup"><span data-stu-id="03938-110">Therefore, quota settings on one volume can be compared to settings on another volume.</span></span>

<span data-ttu-id="03938-111">Hay dos tipos de límites de cuota de disco, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="03938-111">There are two types of disk quota limits, as shown in the following table.</span></span>



| <span data-ttu-id="03938-112">Límite</span><span class="sxs-lookup"><span data-stu-id="03938-112">Limit</span></span>                        | <span data-ttu-id="03938-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="03938-113">Description</span></span>                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03938-114">Umbral de advertencia</span><span class="sxs-lookup"><span data-stu-id="03938-114">Warning threshold</span></span><br/> | <span data-ttu-id="03938-115">Puede configurar el sistema para que genere una entrada de archivo de registro del sistema cuando el espacio en disco que se carga al usuario supere este valor.</span><span class="sxs-lookup"><span data-stu-id="03938-115">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="03938-116">Cuota máxima</span><span class="sxs-lookup"><span data-stu-id="03938-116">Hard quota</span></span><br/>        | <span data-ttu-id="03938-117">Puede configurar el sistema para que genere una entrada de archivo de registro del sistema cuando el espacio en disco que se carga al usuario supere este valor.</span><span class="sxs-lookup"><span data-stu-id="03938-117">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span> <span data-ttu-id="03938-118">También puede configurar el sistema para que deniegue espacio en disco adicional al usuario cuando el espacio en disco que se carga al usuario supere este valor.</span><span class="sxs-lookup"><span data-stu-id="03938-118">You can also configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.</span></span><br/> |



 

<span data-ttu-id="03938-119">El sistema de archivos NTFS crea automáticamente una entrada de cuota de usuario la primera vez que un usuario escribe en el volumen.</span><span class="sxs-lookup"><span data-stu-id="03938-119">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="03938-120">A las entradas creadas automáticamente se les asignan los valores de umbral de advertencia y límite de cuota máxima predeterminados para el volumen.</span><span class="sxs-lookup"><span data-stu-id="03938-120">Entries that are created automatically are assigned the default warning threshold and hard quota limit values for the volume.</span></span>

 

 




