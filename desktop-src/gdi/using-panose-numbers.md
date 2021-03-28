---
description: Los archivos de fuente TrueType incluyen números Panose, que las aplicaciones pueden usar para elegir una fuente que se ajuste a sus especificaciones.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Usar números Panose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278514"
---
# <a name="using-panose-numbers"></a>Usar números Panose

Los archivos de fuente TrueType incluyen números Panose, que las aplicaciones pueden usar para elegir una fuente que se ajuste a sus especificaciones. El sistema Panose clasifica caras por 10 atributos diferentes. Para obtener más información acerca de estos atributos, vea [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose). Una estructura **PAnose** forma parte de la estructura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (cuyos valores se rellenan mediante una llamada a la función [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).

Los atributos Panose se clasifican individualmente en una escala. Los valores resultantes se concatenan para generar un número. Dado este número para una fuente y una métrica matemática para medir las distancias en el espacio de la Panose, una aplicación puede determinar los vecinos más cercanos.

 

 



