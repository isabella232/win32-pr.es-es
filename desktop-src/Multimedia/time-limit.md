---
title: Límite de tiempo
description: Límite de tiempo
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Estructura CAPTUREPARMS
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Estructura CAPTUREPARMS
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779975"
---
# <a name="time-limit"></a><span data-ttu-id="fcec6-109">Límite de tiempo</span><span class="sxs-lookup"><span data-stu-id="fcec6-109">Time Limit</span></span>

<span data-ttu-id="fcec6-110">Puede limitar la duración de una operación de captura mediante los miembros **fLimitEnabled** y **wTimeLimit** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="fcec6-110">You can limit the duration of a capture operation by using the **fLimitEnabled** and **wTimeLimit** members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="fcec6-111">El miembro **fLimitEnabled** indica si se va a establecer el tiempo de la operación de captura, mientras que **wTimeLimit** especifica la duración máxima de la operación de captura.</span><span class="sxs-lookup"><span data-stu-id="fcec6-111">The **fLimitEnabled** member indicates whether the capture operation is to be timed, while **wTimeLimit** specifies the maximum duration of the capture operation.</span></span>

<span data-ttu-id="fcec6-112">Puede recuperar los valores de **fLimitEnabled** y **wTimeLimit** mediante el mensaje de [**configuración de la secuencia de \_ \_ \_ salida \_ Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="fcec6-112">You can retrieve the values for **fLimitEnabled** and **wTimeLimit** by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="fcec6-113">Puede habilitar un temporizador para la operación de captura especificando **true** como el valor de **fLimitEnabled**, o bien puede establecer la duración de la operación de captura especificando un valor, en segundos, para **wTimeLimit**.</span><span class="sxs-lookup"><span data-stu-id="fcec6-113">You can enable a timer for the capture operation by specifying **TRUE** as the value of **fLimitEnabled**, or you can set the duration of the capture operation by specifying a value, in seconds, for **wTimeLimit**.</span></span> <span data-ttu-id="fcec6-114">Después de establecer estos miembros, envíe la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) actualizada a la ventana de captura mediante el mensaje de configuración de la secuencia de definición de [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Cap de [**WM \_ \_ \_ \_**](wm-cap-set-sequence-setup.md) (o la macro capCaptureSetSetup).</span><span class="sxs-lookup"><span data-stu-id="fcec6-114">After you set these members, send the updated [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="fcec6-115">El valor predeterminado de **fLimitEnabled** es **false**.</span><span class="sxs-lookup"><span data-stu-id="fcec6-115">The default value of **fLimitEnabled** is **FALSE**.</span></span>

 

 




