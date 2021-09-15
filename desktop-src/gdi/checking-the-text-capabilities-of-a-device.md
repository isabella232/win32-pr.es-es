---
description: Puede usar las funciones EnumFonts y EnumFontFamilies para enumerar las fuentes disponibles en un contexto de dispositivo de memoria compatible con la impresora.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Comprobación de las funcionalidades de texto de un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569553"
---
# <a name="checking-the-text-capabilities-of-a-device"></a>Comprobación de las funcionalidades de texto de un dispositivo

Puede usar las funciones [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) y [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) para enumerar las fuentes disponibles en un contexto de dispositivo de memoria compatible con la impresora. También puede usar la función [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar información sobre las funcionalidades de texto de un dispositivo. Al llamar a [**la función GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) con el índice NUMFONTS, puede determinar el número mínimo de fuentes admitidas por una impresora. (Una impresora individual puede admitir más fuentes de las especificadas en el valor devuelto de **GetDeviceCaps** con el índice NUMFONTS). Mediante el índice TEXTCAPS, puede identificar muchas de las funcionalidades de texto del dispositivo especificado.

 

 
