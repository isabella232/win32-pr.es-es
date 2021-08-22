---
description: Las paletas de medio tono están diseñadas para usarse cada vez que el modo de ajuste de un contexto de dispositivo se establece en HALFTONE.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Paleta de medio tono y ajuste de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be13f780dc5496173ffb4ddb990a96f7dbe462223e41e8a48d4a58329451277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761009"
---
# <a name="halftone-palette-and-color-adjustment"></a>Paleta de medio tono y ajuste de color

Las paletas de medio tono están diseñadas para usarse cada vez que el modo de ajuste de un contexto de dispositivo se establece en HALFTONE. Una aplicación crea una paleta de medio tono mediante la [**función CreateHalftonePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) La aplicación debe seleccionar y realizar esta paleta en el contexto del dispositivo antes de llamar a la función [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) o [**StretchDIBits.**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

El sistema ajusta automáticamente el color de entrada de los mapas de bits de origen cada vez que las aplicaciones llaman a las funciones [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) y [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) y el modo de ajuste de un contexto de dispositivo se establece en HALFTONE. Estos ajustes de color afectan a determinados atributos de la imagen, como el contraste y el brillo. Una aplicación puede establecer los valores de ajuste de color mediante la [**función SetColorAdjustment.**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) La aplicación puede recuperar los valores de ajuste de color para el contexto de dispositivo especificado mediante la [**función GetColorAdjustment.**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment)

 

 



