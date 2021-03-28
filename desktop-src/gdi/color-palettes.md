---
description: Una paleta de colores es una matriz que contiene valores de color que identifican los colores que se pueden mostrar o dibujar actualmente en el dispositivo de salida.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Paletas de colores (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155657"
---
# <a name="color-palettes-windows-gdi"></a>Paletas de colores (Windows GDI)

Una paleta de colores es una matriz que contiene valores de color que identifican los colores que se pueden mostrar o dibujar actualmente en el dispositivo de salida. Las paletas de colores las utilizan los dispositivos que son capaces de generar muchos colores, pero que solo pueden mostrar o dibujar un subconjunto de ellos en un momento dado. Para estos dispositivos, el sistema mantiene una *paleta del sistema* para realizar un seguimiento de los colores actuales del dispositivo y administrarlos. Las aplicaciones no tienen acceso directo a la paleta del sistema. En su lugar, el sistema asocia una paleta predeterminada con cada contexto de dispositivo. Las aplicaciones pueden usar los colores de la paleta predeterminada o definir sus propios colores creando *paletas lógicas* y asociándolos con contextos de dispositivo individuales.

Una aplicación puede determinar si un dispositivo admite las paletas de colores comprobando el \_ bit de la paleta RC en el valor RASTERCAPS devuelto por la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .

 

 



