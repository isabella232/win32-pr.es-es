---
description: El \_ tipo de DataType Initialize de negociación es un valor especial de tipo DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a55879a0952d3f8b5e268ec6a01a666bdbf5ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811215"
---
# <a name="initialize_negotiation"></a><span data-ttu-id="45daf-103">INICIALIZAr \_ negociación</span><span class="sxs-lookup"><span data-stu-id="45daf-103">INITIALIZE\_NEGOTIATION</span></span>

<span data-ttu-id="45daf-104">El tipo de DataType **Initialize de \_ negociación** es un valor especial de tipo **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="45daf-104">The **INITIALIZE\_NEGOTIATION** datatype is a special value of type **DWORD**.</span></span> <span data-ttu-id="45daf-105">Se puede pasar como el parámetro *dwDeviceID* en las funciones [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) y [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) .</span><span class="sxs-lookup"><span data-stu-id="45daf-105">It can be passed as the *dwDeviceID* parameter in the [**TSPI\_lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) and [**TSPI\_phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) functions.</span></span> <span data-ttu-id="45daf-106">Esto indica que TAPI puede negociar un número de versión de la interfaz TSPI independientemente de cualquier dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="45daf-106">Doing so indicates that TAPI can negotiate a TSPI interface version number independent of any specific devices.</span></span>

 

 
