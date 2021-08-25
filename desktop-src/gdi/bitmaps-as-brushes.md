---
description: Varias funciones usan el pincel seleccionado actualmente en un contexto de dispositivo para realizar operaciones de mapa de bits.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Mapas de bits como pinceles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8e218180ab646de1c9c8ff622be1bcc268df73f6f4bb0b6df82482c9a2c851
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944255"
---
# <a name="bitmaps-as-brushes"></a>Mapas de bits como pinceles

Varias funciones usan el pincel seleccionado actualmente en un contexto de dispositivo para realizar operaciones de mapa de bits. Por ejemplo, la función [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) replica el pincel en una región rectangular dentro de una ventana y la función [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica el pincel dentro de un área de una ventana delimitada por el color especificado (a diferencia de **PatBlt,** **FloodFill** rellena formas norectangulares).

La [**función FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica el pincel dentro de una región delimitada por un color especificado. Sin embargo, a diferencia [**de la función PatBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) **FloodFill** no combina los datos de color del pincel con los datos de color de los píxeles de la pantalla; simplemente establece el color de todos los píxeles dentro de la región incluida en la pantalla en el color del pincel que está seleccionado actualmente en el contexto del dispositivo.

 

 



