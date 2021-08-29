---
title: Acceso y control de datos de fotogramas DWM
description: En este tema se de Administrador de ventanas de escritorio API de almacenamiento de datos (DWM) que se usan para la programación y la presentación multimedia.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Administrador de ventanas de escritorio (DWM), API de programación y presentación multimedia
- DWM (Administrador de ventanas de escritorio), API de programación y presentación multimedia
- API de programación y presentación multimedia
- Administrador de ventanas de escritorio (DWM),acceso a los datos de fotogramas
- DWM (Administrador de ventanas de escritorio), acceso a los datos de fotogramas
- acceso a los datos de fotogramas
- Administrador de ventanas de escritorio (DWM), controlar los datos de fotogramas
- DWM (Administrador de ventanas de escritorio), controlar los datos de fotogramas
- controlar los datos de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4cc9195a6c6032ee467f9d353b1dc57c1be0a03781a3b695ccb5453965f8cfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787315"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a>Acceso y control de datos de fotogramas DWM

En este tema se de Administrador de ventanas de escritorio API de almacenamiento de datos (DWM) que se usan para la programación y la presentación multimedia.

## <a name="dwm-frame-timing-api"></a>DWM Frame Timing API

Las API de programación y presentación multimedia permiten un control más detallado de cuándo se compone y se presenta la imagen de escritorio. Esto suele ser necesario para las aplicaciones de reproducción de vídeo y multimedia para las que dwm se ejecuta de forma asincrónica con su propia programación de presentación, lo que puede dar lugar a artefactos de muestreo si no están estrechamente controlados.

Las funciones de programación y presentación multimedia incluyen lo siguiente. Los detalles de su uso se encuentran en esas páginas.

-   [**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss). Notifica al DWM que habilite la programación del Servicio de programación de clases multimedia (MMCSS) mientras el proceso de llamada está activo.
-   [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo). Recupera la información de control de tiempo de composición actual.
-   [**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration). Cambia el número de actualizaciones durante las que se mostrará el fotograma anterior.
-   [**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration). Establece el número de actualizaciones en las que se va a mostrar el marco presentado.
-   [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters). Establece los parámetros actuales para la composición de fotogramas.

 

 




