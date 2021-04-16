---
description: Hay una serie de tipos de copia de seguridad admitidos por Convención&\# 8212; incremental, diferencial y completo&\# 8212; compatible con VSS, así como una configuración de copia de seguridad con respecto a VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configuraciones de copia de seguridad de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696471"
---
# <a name="vss-backup-configurations"></a><span data-ttu-id="3b6ce-103">Configuraciones de copia de seguridad de VSS</span><span class="sxs-lookup"><span data-stu-id="3b6ce-103">VSS Backup Configurations</span></span>

<span data-ttu-id="3b6ce-104">Hay una serie de tipos de copia de seguridad admitidos por Convención (incremental, diferencial y completo) que VSS es consciente de, así como una configuración de copia de seguridad que se da a VSS.</span><span class="sxs-lookup"><span data-stu-id="3b6ce-104">There are a number of conventionally supported backup types—incremental, differential, and full—that VSS is aware of, as well as a backup configuration peculiar to VSS.</span></span>

<span data-ttu-id="3b6ce-105">Al definir una configuración de copia de seguridad, un solicitante y los escritores de un sistema indican cómo se escribirán los datos en un dispositivo de almacenamiento, cómo se implementará el mecanismo de instantáneas y qué información se debe guardar.</span><span class="sxs-lookup"><span data-stu-id="3b6ce-105">In defining a backup configuration, a requester and the writers on a system indicate how data will be written to a storage device, how the shadow copy mechanism will be deployed, and what information needs to be saved.</span></span> <span data-ttu-id="3b6ce-106">La interacción entre escritores y solicitantes viene determinada por el tipo de copia de seguridad que un solicitante desea realizar y por los tipos (o esquemas) que admite cada escritor:</span><span class="sxs-lookup"><span data-stu-id="3b6ce-106">Interaction between writers and requesters is determined by the type of backup a requester wants to perform and the kinds (or schemas) that each writer can support:</span></span>

-   [<span data-ttu-id="3b6ce-107">Estado de copia de seguridad de VSS</span><span class="sxs-lookup"><span data-stu-id="3b6ce-107">VSS Backup State</span></span>](vss-backup-state.md)
-   [<span data-ttu-id="3b6ce-108">Compatibilidad con el esquema de copia de seguridad del escritor</span><span class="sxs-lookup"><span data-stu-id="3b6ce-108">Writer Backup Schema Support</span></span>](writer-backup-schema-support.md)
-   [<span data-ttu-id="3b6ce-109">Compatibilidad con esquemas de nivel de archivo</span><span class="sxs-lookup"><span data-stu-id="3b6ce-109">File Level Schema Support</span></span>](file-level-schema-support.md)

 

 



