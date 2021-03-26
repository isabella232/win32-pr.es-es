---
description: Las paletas de semitonos están pensadas para usarse siempre que el modo de estiramiento de un contexto de dispositivo se establezca en semitonos.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Paleta de semitono y ajuste de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544478"
---
# <a name="halftone-palette-and-color-adjustment"></a>Paleta de semitono y ajuste de color

Las paletas de semitonos están pensadas para usarse siempre que el modo de estiramiento de un contexto de dispositivo se establezca en semitonos. Una aplicación crea una paleta de semitonos mediante la función [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) . La aplicación debe seleccionar y obtener esta paleta en el contexto del dispositivo antes de llamar a la función [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .

El sistema ajusta automáticamente el color de entrada de los mapas de bits de origen cada vez que las aplicaciones llaman a las funciones [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) y [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) y el modo de ajuste de un contexto de dispositivo se establece en semitonos. Estos ajustes de color afectan a ciertos atributos de la imagen, como el contraste y el brillo. Una aplicación puede establecer los valores de ajuste de color mediante la función [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) . La aplicación puede recuperar los valores de ajuste de color para el contexto de dispositivo especificado mediante la función [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .

 

 



