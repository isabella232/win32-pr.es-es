---
description: Un polígono es una forma rellena con lados rectas.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Acerca de los polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0d28bd915237991294f6579448ca08785481f374814f0ed5840f77ee9f813c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966445"
---
# <a name="about-polygons"></a>Acerca de los polígonos

Un *polígono* es una forma rellena con lados rectas. Los lados de un polígono se dibujan mediante el lápiz actual. Cuando el sistema rellena un polígono, usa el pincel actual y el modo de relleno del polígono actual. Los dos modos de relleno, alternativo (valor predeterminado) y sinuoso, determinan si las regiones dentro de un polígono complejo se rellenan o se deja sin dibujar. Una aplicación puede seleccionar cualquiera de los modos llamando a la [**función SetPolyFillMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) Para obtener más información sobre los modos de relleno de polígono, vea [Regiones](regions.md).

En la ilustración siguiente se muestra un polígono dibujado mediante [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).

![ilustración de un polígono en forma de una estrella de cinco puntas](images/csfsh-04.png)

Además de dibujar un único polígono mediante [**Polygon,**](/windows/win32/api/wingdi/nf-wingdi-polygon)una aplicación puede dibujar varios polígonos mediante la [**función PolyPolygon.**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)

 

 
