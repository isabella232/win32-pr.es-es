---
description: Puede usar las funciones EnumFonts y EnumFontFamilies para enumerar las fuentes disponibles en un contexto de dispositivo de memoria compatible con la impresora.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Comprobación de las funcionalidades de texto de un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7121e7b5e2a416d06d79dba33c9a7c2eb7f6fb26d766a30b383f024e87e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119354855"
---
# <a name="checking-the-text-capabilities-of-a-device"></a>Comprobación de las funcionalidades de texto de un dispositivo

Puede usar las funciones [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) y [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) para enumerar las fuentes disponibles en un contexto de dispositivo de memoria compatible con la impresora. También puede usar la función [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar información sobre las funcionalidades de texto de un dispositivo. Al llamar a [**la función GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) con el índice NUMFONTS, puede determinar el número mínimo de fuentes admitidas por una impresora. (Una impresora individual puede admitir más fuentes de las especificadas en el valor devuelto de **GetDeviceCaps** con el índice NUMFONTS). Mediante el índice TEXTCAPS, puede identificar muchas de las funcionalidades de texto del dispositivo especificado.

 

 
