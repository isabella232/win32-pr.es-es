---
description: Las funciones siguientes se usan con pinceles.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Funciones de pincel (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44f122592e1f13186253b349089706686d352460a364e405c404fd326f64989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849295"
---
# <a name="brush-functions-windows-gdi"></a>Funciones de pincel (Windows GDI)

Las funciones siguientes se usan con pinceles.



| Función                                                   | Descripción                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | Crea un pincel con un estilo, color y patrón especificados. |
| [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | Crea un pincel con el patrón a partir de una DIB.                |
| [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | Crea un pincel con un patrón de sombreado y un color             |
| [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | Crea un pincel con un patrón de mapa de bits                      |
| [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | Crea un pincel con un color sólido                         |
| [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | Obtiene el origen del pincel para un contexto de dispositivo.                 |
| [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | Obtiene un identificador de un pincel que corresponde a un índice de color |
| [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | Pinta un rectángulo                                         |
| [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | Establece el origen del pincel para un contexto de dispositivo.                 |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Establece el color actual del pincel del contexto del dispositivo.               |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Las siguientes funciones solo se proporcionan para la compatibilidad con versiones de 16 bits de Windows.

[**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



