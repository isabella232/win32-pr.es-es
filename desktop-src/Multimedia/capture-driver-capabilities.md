---
title: Capacidades del controlador de captura
description: Capacidades del controlador de captura
ms.assetid: 6e74635e-9dac-419d-a264-08fee04ae7b7
keywords:
- Mensaje WM_CAP_DRIVER_GET_CAPS
- capDriverGetCaps (macro)
- Estructura CAPDRIVERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87fb4f9cb439229721b6c10aa6207af601f9ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075322"
---
# <a name="capture-driver-capabilities"></a><span data-ttu-id="38dba-106">Capacidades del controlador de captura</span><span class="sxs-lookup"><span data-stu-id="38dba-106">Capture Driver Capabilities</span></span>

<span data-ttu-id="38dba-107">Puede recuperar las capacidades de hardware del controlador de captura conectado actualmente mediante el mensaje [**de \_ \_ \_ obtención \_ de Cap del controlador Cap de WM**](wm-cap-driver-get-caps.md) (o la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) ).</span><span class="sxs-lookup"><span data-stu-id="38dba-107">You can retrieve the hardware capabilities of the currently connected capture driver by using the [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message (or the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro).</span></span> <span data-ttu-id="38dba-108">Este mensaje devuelve las capacidades del controlador de captura y el hardware subyacente en la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="38dba-108">This message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

 

 




