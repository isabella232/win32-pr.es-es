---
description: TSPIMessage es un tipo de enumeración que define el conjunto de funciones LINEEVENT y PHONEEVENT adicionales que aparecen en TSPI que no aparecen en TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811438"
---
# <a name="tspimessage"></a><span data-ttu-id="ccec9-103">TSPIMessage</span><span class="sxs-lookup"><span data-stu-id="ccec9-103">TSPIMessage</span></span>

<span data-ttu-id="ccec9-104">**TSPIMessage** es un tipo de enumeración que define el conjunto de funciones [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) y [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) adicionales que aparecen en TSPI que no aparecen en TAPI.</span><span class="sxs-lookup"><span data-stu-id="ccec9-104">**TSPIMessage** is an enumeration type that defines the set of additional [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) and [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) functions appearing in TSPI that do not appear in TAPI.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccec9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccec9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccec9-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_base de mensaje de TSPI \_</span><span class="sxs-lookup"><span data-stu-id="ccec9-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI\_MESSAGE\_BASE</span></span>
</dt> <dd>

<span data-ttu-id="ccec9-107">El número más bajo del intervalo de valores de mensaje específicos de TSPI.</span><span class="sxs-lookup"><span data-stu-id="ccec9-107">The lowest number in the range of TSPI-specific message values.</span></span> <span data-ttu-id="ccec9-108">Este valor no tiene ningún significado por sí solo, pero sirve como base para definir los demás valores.</span><span class="sxs-lookup"><span data-stu-id="ccec9-108">This value has no meaning by itself, but serves as a base for defining the other values.</span></span>

</dd> <dt>

<span data-ttu-id="ccec9-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LÍNEA \_ NEWCALL</span><span class="sxs-lookup"><span data-stu-id="ccec9-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE\_NEWCALL</span></span>
</dt> <dd>

<span data-ttu-id="ccec9-110">Especifica que ha llegado una nueva llamada entrante y la introduce en TAPI.</span><span class="sxs-lookup"><span data-stu-id="ccec9-110">Specifies that a new, incoming call has arrived and introduces it to TAPI.</span></span> <span data-ttu-id="ccec9-111">Este debe ser el primer mensaje enviado a TAPI para una nueva llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="ccec9-111">This must be the first message sent to TAPI for a new incoming call.</span></span> <span data-ttu-id="ccec9-112">TAPI devuelve su identificador opaco para la llamada como parte de su control de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="ccec9-112">TAPI returns its opaque identifier for the call as part of its handling of this message.</span></span>

</dd> <dt>

<span data-ttu-id="ccec9-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LÍNEA \_ CALLDEVSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="ccec9-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE\_CALLDEVSPECIFIC</span></span>
</dt> <dd>

<span data-ttu-id="ccec9-114">Especifica que se ha producido un evento específico del dispositivo en un dispositivo de llamada.</span><span class="sxs-lookup"><span data-stu-id="ccec9-114">Specifies that a device-specific event has occurred on a call device.</span></span>

</dd> <dt>

<span data-ttu-id="ccec9-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LÍNEA \_ CALLDEVSPECIFICFEATURE</span><span class="sxs-lookup"><span data-stu-id="ccec9-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE\_CALLDEVSPECIFICFEATURE</span></span>
</dt> <dd>

<span data-ttu-id="ccec9-116">Especifica que se ha producido un evento de característica específico del dispositivo en un dispositivo de llamada.</span><span class="sxs-lookup"><span data-stu-id="ccec9-116">Specifies that a device-specific feature event has occurred on a call device.</span></span>

</dd> </dl>

 

 
