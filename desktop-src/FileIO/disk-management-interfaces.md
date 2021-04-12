---
description: Interfaces usadas en administración de discos.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de administración de discos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278462"
---
# <a name="disk-management-interfaces"></a><span data-ttu-id="70886-103">Interfaces de administración de discos</span><span class="sxs-lookup"><span data-stu-id="70886-103">Disk Management Interfaces</span></span>

<span data-ttu-id="70886-104">En administración de discos se usan las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="70886-104">The following interfaces are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="70886-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="70886-105">In this section</span></span>



| <span data-ttu-id="70886-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="70886-106">Interface</span></span>                                                     | <span data-ttu-id="70886-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="70886-107">Description</span></span>                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70886-108">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="70886-108">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | <span data-ttu-id="70886-109">Controla las instalaciones de cuota de disco de un solo volumen del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="70886-109">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="70886-110">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="70886-110">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | <span data-ttu-id="70886-111">Recibe notificaciones de eventos relacionados con la cuota.</span><span class="sxs-lookup"><span data-stu-id="70886-111">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="70886-112">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="70886-112">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | <span data-ttu-id="70886-113">Representa una única entrada de cuota de usuario en el archivo de información de cuota de volumen.</span><span class="sxs-lookup"><span data-stu-id="70886-113">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="70886-114">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="70886-114">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | <span data-ttu-id="70886-115">Agrega varios objetos de usuario de cuota a un contenedor que se envía para su actualización en una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="70886-115">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="70886-116">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="70886-116">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | <span data-ttu-id="70886-117">Enumera las entradas de cuota de usuario en el volumen.</span><span class="sxs-lookup"><span data-stu-id="70886-117">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

