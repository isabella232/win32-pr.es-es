---
description: Una paleta de colores es una matriz que contiene valores de color que identifican los colores que se pueden mostrar o dibujar actualmente en el dispositivo de salida.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Paletas de colores (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81079ac94b40de98bc1c53098a8b9d1654f90d0d855397ac38d11311e9741e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761962"
---
# <a name="color-palettes-windows-gdi"></a>Paletas de colores (Windows GDI)

Una paleta de colores es una matriz que contiene valores de color que identifican los colores que se pueden mostrar o dibujar actualmente en el dispositivo de salida. Las paletas de colores se usan en dispositivos que son capaces de generar muchos colores, pero que solo pueden mostrar o dibujar un subconjunto de estos en un momento dado. Para estos dispositivos, el sistema mantiene una paleta *del sistema* para realizar un seguimiento y administrar los colores actuales del dispositivo. Las aplicaciones no tienen acceso directo a la paleta del sistema. En su lugar, el sistema asocia una paleta predeterminada con cada contexto de dispositivo. Las aplicaciones pueden usar los colores de la paleta predeterminada o definir sus propios colores mediante la creación de *paletas lógicas* y su asociación a contextos de dispositivo individuales.

Una aplicación puede determinar si un dispositivo admite paletas de colores mediante la comprobación del bit RC PALETTE en el valor RASTERCAPS devuelto por \_ la [**función GetDeviceCaps.**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)

 

 



