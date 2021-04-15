---
description: Interfaces utilizadas con cuotas de disco.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Interfaces de cuota de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497969"
---
# <a name="disk-quota-interfaces"></a><span data-ttu-id="6143f-103">Interfaces de cuota de disco</span><span class="sxs-lookup"><span data-stu-id="6143f-103">Disk Quota Interfaces</span></span>

<span data-ttu-id="6143f-104">Las siguientes interfaces se utilizan con cuotas de disco.</span><span class="sxs-lookup"><span data-stu-id="6143f-104">The following interfaces are used with disk quotas.</span></span>



| <span data-ttu-id="6143f-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="6143f-105">Interface</span></span>                                          | <span data-ttu-id="6143f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6143f-106">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6143f-107">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="6143f-107">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | <span data-ttu-id="6143f-108">Controla las instalaciones de cuota de disco de un solo volumen del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="6143f-108">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="6143f-109">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="6143f-109">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | <span data-ttu-id="6143f-110">Recibe notificaciones de eventos relacionados con la cuota.</span><span class="sxs-lookup"><span data-stu-id="6143f-110">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="6143f-111">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="6143f-111">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | <span data-ttu-id="6143f-112">Representa una única entrada de cuota de usuario en el archivo de información de cuota de volumen.</span><span class="sxs-lookup"><span data-stu-id="6143f-112">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="6143f-113">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="6143f-113">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | <span data-ttu-id="6143f-114">Agrega varios objetos de usuario de cuota a un contenedor que se envía para su actualización en una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="6143f-114">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="6143f-115">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="6143f-115">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | <span data-ttu-id="6143f-116">Enumera las entradas de cuota de usuario en el volumen.</span><span class="sxs-lookup"><span data-stu-id="6143f-116">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

