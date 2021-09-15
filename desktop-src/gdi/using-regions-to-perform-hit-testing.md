---
description: En el ejemplo de Brushes se usan regiones para simular un mapa de bits monocromo de \# &0034;zoomed&0034; vista de un mapa de bits monocromo de 8 x \# 8 píxeles.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Uso de regiones para realizar pruebas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474312"
---
# <a name="using-regions-to-perform-hit-testing"></a>Uso de regiones para realizar pruebas de acceso

En el ejemplo de Brushes se usan [regiones](brushes.md) para simular una vista "ampliada" de un mapa de bits monocromo de 8 por 8 píxeles. Al hacer clic en los píxeles de este mapa de bits, el usuario crea un pincel personalizado adecuado para las operaciones de dibujo. En el ejemplo se muestra cómo usar la [**función PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) para realizar pruebas de acceso y la función [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) para invertir los colores de una región.

 

 



