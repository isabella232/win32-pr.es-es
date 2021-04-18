---
description: Las siguientes funciones se usan con los pinceles.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Funciones de pincel (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544550"
---
# <a name="brush-functions-windows-gdi"></a>Funciones de pincel (Windows GDI)

Las siguientes funciones se usan con los pinceles.



| Función                                                   | Descripción                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | Crea un pincel con un estilo, color y patrón especificados |
| [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | Crea un pincel con el modelo a partir de un DIB                |
| [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | Crea un pincel con un patrón de trama y un color             |
| [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | Crea un pincel con un modelo de mapa de bits.                      |
| [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | Crea un pincel con un color sólido.                         |
| [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | Obtiene el origen del pincel para un contexto de dispositivo.                 |
| [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | Obtiene un identificador para un pincel que corresponde a un índice de color. |
| [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | Dibuja un rectángulo.                                         |
| [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | Establece el origen del pincel para un contexto de dispositivo                 |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Establece el color del pincel de contexto del dispositivo actual.               |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Las siguientes funciones solo se proporcionan por compatibilidad con las versiones de 16 bits de Windows.

[**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



