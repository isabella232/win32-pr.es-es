---
description: Las operaciones de copia de seguridad y restauración de VSS usan un protocolo para la interacción de los sistemas que utilizan almacenamiento masivo (escritores) y los que lo respaldan (solicitantes).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Usar el Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541763"
---
# <a name="using-the-volume-shadow-copy-service"></a><span data-ttu-id="7b3de-103">Usar el Servicio de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="7b3de-103">Using the Volume Shadow Copy Service</span></span>

<span data-ttu-id="7b3de-104">Las operaciones de copia de seguridad y restauración de VSS usan un protocolo para la interacción de los sistemas que utilizan almacenamiento masivo (escritores) y los que lo respaldan (solicitantes).</span><span class="sxs-lookup"><span data-stu-id="7b3de-104">VSS backup and restore operations each use a protocol for the interaction of the systems that use mass storage (writers) and those that back it up (requesters).</span></span>

<span data-ttu-id="7b3de-105">Las operaciones de copia de seguridad y restauración están dirigidas principalmente por el solicitante, que controla el comportamiento del escritor y del proveedor mediante la generación de eventos COM en todo el sistema para que los procese el escritor.</span><span class="sxs-lookup"><span data-stu-id="7b3de-105">Both backup and restore operations are primarily driven by the requester, which controls writer and provider behavior by generating systemwide COM events for the writer to process.</span></span> <span data-ttu-id="7b3de-106">Dado que los métodos de generación de eventos son asincrónicos, los escritores tienen un control limitado en el estado del solicitante a través de los controladores asincrónicos disponibles para VSS (vea [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span><span class="sxs-lookup"><span data-stu-id="7b3de-106">Because event-generating methods are asynchronous, writers do have limited control into the requester's state through the asynchronous handlers available to VSS (see [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span></span>

<span data-ttu-id="7b3de-107">Esta interacción requiere estructuras de datos básicas que describen archivos y grupos de archivos ([*componentes*](vssgloss-c.md)), así como un modelo de metadatos para permitir el almacenamiento de la información de copia de seguridad y permitir la comunicación entre el autor y el solicitante.</span><span class="sxs-lookup"><span data-stu-id="7b3de-107">This interaction requires basic data structures describing files and groups of files ([*components*](vssgloss-c.md)), as well as a metadata model to allow the storage of backup information and to permit writer/requester communication.</span></span>

-   [<span data-ttu-id="7b3de-108">Compatibilidad de aplicaciones de VSS</span><span class="sxs-lookup"><span data-stu-id="7b3de-108">VSS Application Compatibility</span></span>](usage-conventions.md)
-   [<span data-ttu-id="7b3de-109">Configuración de VSS</span><span class="sxs-lookup"><span data-stu-id="7b3de-109">Configuring VSS</span></span>](configuring-vss.md)
-   [<span data-ttu-id="7b3de-110">Metadatos de VSS</span><span class="sxs-lookup"><span data-stu-id="7b3de-110">VSS Metadata</span></span>](vss-metadata.md)
-   [<span data-ttu-id="7b3de-111">Trabajar con la selección y las rutas de acceso lógicas</span><span class="sxs-lookup"><span data-stu-id="7b3de-111">Working with Selectability and Logical Paths</span></span>](working-with-selectability-and-logical-paths.md)
-   [<span data-ttu-id="7b3de-112">Información general sobre el procesamiento de una copia de seguridad en VSS</span><span class="sxs-lookup"><span data-stu-id="7b3de-112">Overview of Processing a Backup Under VSS</span></span>](overview-of-processing-a-backup-under-vss.md)
-   [<span data-ttu-id="7b3de-113">Información general sobre el procesamiento de una restauración en VSS</span><span class="sxs-lookup"><span data-stu-id="7b3de-113">Overview of Processing a Restore Under VSS</span></span>](overview-of-processing-a-restore-under-vss.md)

 

 



