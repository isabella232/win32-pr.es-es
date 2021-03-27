---
description: Un polígono es una forma rellena con lados rectos.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Acerca de los polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082371"
---
# <a name="about-polygons"></a>Acerca de los polígonos

Un *polígono* es una forma rellena con lados rectos. Los lados de un polígono se dibujan utilizando el lápiz actual. Cuando el sistema rellena un polígono, usa el pincel actual y el modo de relleno de polígono actual. Los dos modos de relleno, alternativos (el valor predeterminado) y el bobinado, determinan si las regiones dentro de un polígono complejo se rellenan o se dejan sin pintar. Una aplicación puede seleccionar cualquier modo llamando a la función [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . Para obtener más información sobre los modos de relleno de polígono, consulte [regiones](regions.md).

En la ilustración siguiente se muestra un polígono dibujado mediante [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).

![Ilustración de un polígono en la forma de una estrella de cinco puntas](images/csfsh-04.png)

Además de dibujar un solo polígono con [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), una aplicación puede dibujar varios polígonos mediante la función de [**polipolígono**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .

 

 
