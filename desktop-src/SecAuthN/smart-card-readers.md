---
description: Los lectores son dispositivos estándar en un sistema de tarjeta inteligente. Se controlan a través de controladores y se introducen y se quitan del sistema a través de Plug and Play o a través del elemento dispositivos del panel de control.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lectores de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652934"
---
# <a name="smart-card-readers"></a><span data-ttu-id="171fc-104">Lectores de tarjetas inteligentes</span><span class="sxs-lookup"><span data-stu-id="171fc-104">Smart Card Readers</span></span>

<span data-ttu-id="171fc-105">Los lectores son dispositivos estándar en un sistema de [*tarjeta inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="171fc-105">Readers are standard devices in a [*smart card*](../secgloss/s-gly.md) system.</span></span> <span data-ttu-id="171fc-106">Se controlan a través de controladores y se introducen y se quitan del sistema a través de Plug and Play o a través del elemento dispositivos del panel de control.</span><span class="sxs-lookup"><span data-stu-id="171fc-106">They are controlled through drivers, and are introduced to and removed from the system through Plug and Play or through the Control Panel Devices item.</span></span>

<span data-ttu-id="171fc-107">Cada lector debe definirse para que lo use el [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="171fc-107">Each reader must be defined for use by the [*smart card subsystem*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="171fc-108">El subsistema no es responsable de ningún lector que no se haya asignado específicamente a él.</span><span class="sxs-lookup"><span data-stu-id="171fc-108">The subsystem is not responsible for any reader not specifically given to it.</span></span>

<span data-ttu-id="171fc-109">Los lectores de tarjetas inteligentes se pueden dividir en grupos lógicos denominados grupos de lector.</span><span class="sxs-lookup"><span data-stu-id="171fc-109">Smart card readers can be divided into logical groups called reader groups.</span></span> <span data-ttu-id="171fc-110">El subsistema puede definir estos grupos, así como definidos por los administradores y los usuarios.</span><span class="sxs-lookup"><span data-stu-id="171fc-110">These groups can be defined by the subsystem, as well as defined by administrators and users.</span></span> <span data-ttu-id="171fc-111">Un lector puede pertenecer a más de un grupo de lectores</span><span class="sxs-lookup"><span data-stu-id="171fc-111">A reader can belong to more than one reader group</span></span>

<span data-ttu-id="171fc-112">El subsistema de tarjeta inteligente define los siguientes grupos.</span><span class="sxs-lookup"><span data-stu-id="171fc-112">The smart card subsystem defines the following groups.</span></span>



| <span data-ttu-id="171fc-113">Grupo</span><span class="sxs-lookup"><span data-stu-id="171fc-113">Group</span></span>                | <span data-ttu-id="171fc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="171fc-114">Description</span></span>                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171fc-115">PPAC $ AllReaders</span><span class="sxs-lookup"><span data-stu-id="171fc-115">SCard$AllReaders</span></span>     | <span data-ttu-id="171fc-116">Este grupo contiene todos los lectores del sistema.</span><span class="sxs-lookup"><span data-stu-id="171fc-116">This group contains all the readers in the system.</span></span> <span data-ttu-id="171fc-117">Un nuevo lector proporcionado al subsistema de tarjeta inteligente se incluye automáticamente en el grupo de lectores de todo el sistema, PPAC $ AllReaders.</span><span class="sxs-lookup"><span data-stu-id="171fc-117">A new reader given to the smart card subsystem is automatically included in the system-wide reader group, SCard$AllReaders.</span></span>                         |
| <span data-ttu-id="171fc-118">PPAC $ DefaultReaders</span><span class="sxs-lookup"><span data-stu-id="171fc-118">SCard$DefaultReaders</span></span> | <span data-ttu-id="171fc-119">Este grupo predeterminado, uno para cada [*terminal*](../secgloss/t-gly.md), contiene todos los lectores asignados al terminal que no están reservados para uso específico.</span><span class="sxs-lookup"><span data-stu-id="171fc-119">This default group, one for each [*terminal*](../secgloss/t-gly.md), contains all the readers assigned to the terminal that are not reserved for specific use.</span></span> |



 

 

 
