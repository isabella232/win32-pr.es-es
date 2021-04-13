---
title: Acceso y control de los datos de los marcos de DWM
description: En este tema se describen las API de Administrador de ventanas de escritorio (DWM) que se usan para la programación y la presentación multimedia.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Administrador de ventanas de escritorio (DWM), programación y API de presentación multimedia
- DWM (Administrador de ventanas de escritorio), programación y API de presentación multimedia
- programación y API de presentación multimedia
- Administrador de ventanas de escritorio (DWM), obtener acceso a los datos del marco
- DWM (Administrador de ventanas de escritorio), acceso a los datos del marco
- obtener acceso a los datos del marco
- Administrador de ventanas de escritorio (DWM), controlar los datos del marco
- DWM (Administrador de ventanas de escritorio), controlar los datos del marco
- controlar los datos del marco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357173"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a>Acceso y control de los datos de los marcos de DWM

En este tema se describen las API de Administrador de ventanas de escritorio (DWM) que se usan para la programación y la presentación multimedia.

## <a name="dwm-frame-timing-api"></a>API de temporización de fotogramas de DWM

Las API de programación y presentación multimedia permiten un control más detallado de Cuándo se compone y se presenta la imagen de escritorio. Normalmente, esto es necesario para las aplicaciones de reproducción multimedia y de vídeo para las que el DWM se ejecuta de forma asincrónica con su propia programación de presentación, lo que puede conducir a los artefactos de muestreo si no se controlan estrechamente.

Entre las funciones de presentación multimedia y programación se incluyen las siguientes. Los detalles de su uso se encuentran en esas páginas.

-   [**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss). Notifica a DWM que habilite la programación del servicio de programación de clases multimedia (MMCSS) mientras el proceso de llamada está activo.
-   [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo). Recupera la información de tiempo de composición actual.
-   [**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration). Cambia el número de actualizaciones durante las cuales se mostrará el fotograma anterior.
-   [**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration). Establece el número de actualizaciones en las que se va a mostrar el marco presentado.
-   [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters). Establece los parámetros presentes para la composición de fotogramas.

 

 




