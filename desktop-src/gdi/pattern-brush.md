---
description: Se crea un pincel de patrón (o personalizado) a partir de un mapa de bits definido por la aplicación o un mapa de bits independiente del dispositivo (DIB). Los rectángulos siguientes se pintaron mediante pinceles de patrón diferentes.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pincel de patrón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48b7d5f3bc5c4b0fd86eda28a35bb56f02e5ba998353d36d829a71655aa66f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831525"
---
# <a name="pattern-brush"></a>Pincel de patrón

Se crea un pincel de patrón (o personalizado) a partir de un mapa de bits definido por la aplicación o un mapa de bits independiente del dispositivo (DIB). Los rectángulos siguientes se pintaron mediante pinceles de patrón diferentes.

![ilustración que muestra tres cuadros, cada uno rellenado con un patrón diferente](images/csbru-05.png)

Para crear un pincel de patrón lógico, una aplicación debe crear primero un mapa de bits. Después de crear el mapa de bits, la aplicación puede crear el pincel de patrón lógico llamando a la función [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) o [**CreateDIBPatternBrushPt,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) y proporcionar un identificador que identifique el mapa de bits (o DIB). Los pinceles que aparecen en la ilustración anterior se crearon a partir de mapas de bits monocromáticos. Para obtener una descripción de mapas de bits, DIB y las funciones que los crean, vea [Mapas de bits.](bitmaps.md)

 

 



