---
description: Una paleta de colores es una matriz que contiene valores de color que identifican los colores que se pueden mostrar o dibujar actualmente en el dispositivo de salida.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Paletas de colores (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473146"
---
# <a name="color-palettes-windows-gdi"></a>Paletas de colores (Windows GDI)

Una paleta de colores es una matriz que contiene valores de color que identifican los colores que se pueden mostrar o dibujar actualmente en el dispositivo de salida. Los dispositivos que son capaces de generar muchos colores usan paletas de colores, pero que solo pueden mostrar o dibujar un subconjunto de estos en un momento dado. Para estos dispositivos, el sistema mantiene una paleta *del sistema* para realizar un seguimiento y administrar los colores actuales del dispositivo. Las aplicaciones no tienen acceso directo a la paleta del sistema. En su lugar, el sistema asocia una paleta predeterminada a cada contexto de dispositivo. Las aplicaciones pueden usar los colores de la paleta predeterminada o definir sus propios colores mediante la creación de *paletas lógicas* y su asociación a contextos de dispositivo individuales.

Una aplicación puede determinar si un dispositivo admite paletas de colores mediante la comprobación del bit RC PALETTE en el valor RASTERCAPS devuelto por \_ la [**función GetDeviceCaps.**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)

 

 



