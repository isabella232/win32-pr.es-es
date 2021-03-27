---
description: Puede usar las funciones EnumFonts y EnumFontFamilies para enumerar las fuentes que están disponibles en un contexto de dispositivo de memoria compatible con impresoras.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Comprobar las capacidades de texto de un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997417"
---
# <a name="checking-the-text-capabilities-of-a-device"></a><span data-ttu-id="000a6-103">Comprobar las capacidades de texto de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="000a6-103">Checking the Text Capabilities of a Device</span></span>

<span data-ttu-id="000a6-104">Puede usar las funciones [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) y [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) para enumerar las fuentes que están disponibles en un contexto de dispositivo de memoria compatible con impresoras.</span><span class="sxs-lookup"><span data-stu-id="000a6-104">You can use the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions to enumerate the fonts that are available in a printer-compatible memory device context.</span></span> <span data-ttu-id="000a6-105">También puede usar la función [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar información sobre las capacidades de texto de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="000a6-105">You can also use the [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve information about the text capabilities of a device.</span></span> <span data-ttu-id="000a6-106">Al llamar a la función [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) con el índice NUMFONTS, puede determinar el número mínimo de fuentes que admite una impresora.</span><span class="sxs-lookup"><span data-stu-id="000a6-106">By calling the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function with the NUMFONTS index, you can determine the minimum number of fonts supported by a printer.</span></span> <span data-ttu-id="000a6-107">(Una impresora individual puede admitir más fuentes de las especificadas en el valor devuelto de **GetDeviceCaps** con el índice NUMFONTS). Mediante el índice TEXTCAPS, puede identificar muchas de las capacidades de texto del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="000a6-107">(An individual printer may support more fonts than specified in the return value from **GetDeviceCaps** with the NUMFONTS index.) By using the TEXTCAPS index, you can identify many of the text capabilities of the specified device.</span></span>

 

 
