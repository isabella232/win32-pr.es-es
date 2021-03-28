---
description: En el ejemplo de pinceles se usan regiones para simular una &\# 0034; zoom&\# 0034; vista de un mapa de bits monocromo de 8 por 8 píxeles.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Usar regiones para realizar pruebas de posicionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276453"
---
# <a name="using-regions-to-perform-hit-testing"></a>Usar regiones para realizar pruebas de posicionamiento

En el ejemplo de [pinceles](brushes.md) se usan regiones para simular una vista "alejada" de un mapa de bits monocromo de 8 por 8 píxeles. Al hacer clic en los píxeles de este mapa de bits, el usuario crea un pincel personalizado adecuado para las operaciones de dibujo. En el ejemplo se muestra cómo usar la función [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) para realizar pruebas de posicionamiento y la función [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) para invertir los colores de una región.

 

 



