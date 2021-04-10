---
title: Crear discos con varias sesiones
description: IMAPi es capaz de crear discos de datos de varias sesiones. Hay algunas consideraciones que se deben tener en cuenta al crear un disco de varias sesiones.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268615"
---
# <a name="creating-discs-with-multiple-sessions"></a><span data-ttu-id="713e9-104">Crear discos con varias sesiones</span><span class="sxs-lookup"><span data-stu-id="713e9-104">Creating Discs with Multiple Sessions</span></span>

<span data-ttu-id="713e9-105">IMAPi es capaz de crear discos de datos de varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="713e9-105">IMAPI is capable of creating multi-session data discs.</span></span> <span data-ttu-id="713e9-106">Hay algunas consideraciones que se deben tener en cuenta al crear un disco de varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="713e9-106">There are a few considerations to be aware of when creating a multi-session disc.</span></span>

<span data-ttu-id="713e9-107">El método [**IDiscMaster:: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina si hay un disco de varias sesiones de IMAPI en la unidad activa al establecer.</span><span class="sxs-lookup"><span data-stu-id="713e9-107">The [**IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) method determines whether there is an IMAPI multi-session disc in the active drive upon setting.</span></span> <span data-ttu-id="713e9-108">Si es así, IMAPi entra en modo de sesión múltiple automáticamente.</span><span class="sxs-lookup"><span data-stu-id="713e9-108">If so, IMAPI goes into multi-session mode automatically.</span></span> <span data-ttu-id="713e9-109">El uso de [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) después de que se haya establecido el modo de varias sesiones hace que IMAPI vuelva al modo de sesión única.</span><span class="sxs-lookup"><span data-stu-id="713e9-109">Using [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) after multi-session mode has been established causes IMAPI to return to single-session mode.</span></span> <span data-ttu-id="713e9-110">Esto significa que se requiere un disco en blanco para una grabación de [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) .</span><span class="sxs-lookup"><span data-stu-id="713e9-110">This means that a blank disc is required for a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) burn.</span></span> <span data-ttu-id="713e9-111">Si el disco está en modo de varias sesiones, el mismo disco debe estar en la grabadora activa o se devolverá un código de error de IMAPi \_ E \_ WRONGDISC.</span><span class="sxs-lookup"><span data-stu-id="713e9-111">If the disc is in multi-session mode, the same disc must be in the active recorder or an error code of IMAPI\_E\_WRONGDISC will be returned.</span></span>

<span data-ttu-id="713e9-112">La selección de una grabadora en formato Joliet hace que IMAPi Lea información del disco instalado actualmente. Si el disco es un disco Joliet de IMAPi anterior que tiene espacio para otra sesión, IMAPi se establece automáticamente en modo de varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="713e9-112">Selecting a recorder while in Joliet format causes IMAPI to read information from the currently installed disc. If the disc is a previous IMAPI Joliet disc that has space for another session, IMAPI automatically sets itself to multi-session mode.</span></span> <span data-ttu-id="713e9-113">Este disco debe estar presente en la grabadora activa al llamar a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span><span class="sxs-lookup"><span data-stu-id="713e9-113">This disc must be present in the active recorder when calling [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span></span>

<span data-ttu-id="713e9-114">Cerrar la primera sesión en un disco requiere 21 MB.</span><span class="sxs-lookup"><span data-stu-id="713e9-114">Closing the first session on a disc requires 21 MB.</span></span> <span data-ttu-id="713e9-115">Cada sesión adicional requiere 11 MB para cerrarse.</span><span class="sxs-lookup"><span data-stu-id="713e9-115">Each additional session requires 11 MB to close.</span></span>

 

 




