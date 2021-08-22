---
description: En el ejemplo de Brushes se usan regiones para simular una vista &\# 0034;zoomed&0034; vista de un mapa de bits monocromo de 8 x \# 8 píxeles.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Uso de regiones para realizar pruebas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d553eeaf37b954d0ec9d0b8897df98cf1a513d7ca7212ca82bc376afe1fc7163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558125"
---
# <a name="using-regions-to-perform-hit-testing"></a>Uso de regiones para realizar pruebas de acceso

En el ejemplo [de Brushes](brushes.md) se usan regiones para simular una vista "ampliada" de un mapa de bits monocromo de 8 por 8 píxeles. Al hacer clic en los píxeles de este mapa de bits, el usuario crea un pincel personalizado adecuado para las operaciones de dibujo. En el ejemplo se muestra cómo usar la [**función PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) para realizar pruebas de acceso y la función [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) para invertir los colores en una región.

 

 



