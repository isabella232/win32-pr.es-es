---
title: User-Initiated captura
description: User-Initiated captura
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903714"
---
# <a name="user-initiated-capture"></a><span data-ttu-id="64575-105">User-Initiated captura</span><span class="sxs-lookup"><span data-stu-id="64575-105">User-Initiated Capture</span></span>

<span data-ttu-id="64575-106">Puede recuperar el valor actual de la marca de captura iniciada por el usuario mediante el mensaje de configuración de la [**\_ \_ \_ \_ secuencia Get Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="64575-106">You can retrieve the current value of the user-initiated capture flag by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="64575-107">El valor de la marca se almacena en el miembro **fMakeUserHitOKToCapture** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="64575-107">The value of the flag is stored in the **fMakeUserHitOKToCapture** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="64575-108">Puede proporcionar al usuario un control preciso sobre cuándo iniciar una sesión de captura estableciendo este miembro en **true**.</span><span class="sxs-lookup"><span data-stu-id="64575-108">You can provide the user with precise control over when to start a capture session by setting this member to **TRUE**.</span></span> <span data-ttu-id="64575-109">AVICap muestra un cuadro de diálogo después de asignar todos los búferes de vídeo y audio para una sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="64575-109">AVICap displays a dialog box after allocating all video and audio buffers for a capture session.</span></span> <span data-ttu-id="64575-110">Esto permite al usuario eliminar los retrasos de captura debido a la inicialización del software.</span><span class="sxs-lookup"><span data-stu-id="64575-110">This lets the user eliminate capture delays because of software initialization.</span></span> <span data-ttu-id="64575-111">Si la aplicación usa un número pequeño de búferes de vídeo, es probable que este cuadro de diálogo no sea necesario.</span><span class="sxs-lookup"><span data-stu-id="64575-111">If your application uses a small number of video buffers, this dialog box is probably unnecessary.</span></span> <span data-ttu-id="64575-112">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="64575-112">The default value is **FALSE**.</span></span>

 

 




