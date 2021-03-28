---
description: Un número de funciones usa el pincel seleccionado actualmente en un contexto de dispositivo para realizar operaciones de mapa de bits.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Mapas de bits como pinceles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276021"
---
# <a name="bitmaps-as-brushes"></a>Mapas de bits como pinceles

Un número de funciones usa el pincel seleccionado actualmente en un contexto de dispositivo para realizar operaciones de mapa de bits. Por ejemplo, la función [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) replica el pincel en una región rectangular dentro de una ventana y la función [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica el pincel dentro de un área de una ventana enlazada por el color especificado (a diferencia de **PatBlt**, **FloodFill** no rellena formas no rectangulares).

La función [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica el pincel dentro de una región limitada por un color especificado. Sin embargo, a diferencia de la función [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) , **FloodFill** no combina los datos de color del pincel con los datos de color de los píxeles de la pantalla. simplemente establece el color de todos los píxeles de la región incluida en la pantalla en el color del pincel seleccionado actualmente en el contexto del dispositivo.

 

 



