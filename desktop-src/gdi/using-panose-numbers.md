---
description: Los archivos de fuente TrueType incluyen números PANOSE, que las aplicaciones pueden usar para elegir una fuente que coincida estrechamente con sus especificaciones.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Uso de números PANOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a974a0d1e708cac931e06e386e2df0802cbea79e5c9d499ca460d6deb5b0bab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037463"
---
# <a name="using-panose-numbers"></a>Uso de números PANOSE

Los archivos de fuente TrueType incluyen números PANOSE, que las aplicaciones pueden usar para elegir una fuente que coincida estrechamente con sus especificaciones. El sistema PANOSE clasifica las caras en 10 atributos diferentes. Para obtener más información sobre estos atributos, vea [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose). Una **estructura PANOSE** forma parte de la estructura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (cuyos valores se rellenan llamando a la [**función GetOutlineTextMetrics).**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)

Los atributos PANOSE se valoran individualmente en una escala. Los valores resultantes se concatenan para generar un número. Dado este número para una fuente y una métrica matemática para medir las distancias en el espacio PANOSE, una aplicación puede determinar los vecinos más cercanos.

 

 



