---
title: Tiempo (Windows Multimedia)
description: Control de tiempo
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib,timing
- Función DrawDibTime
- DrawDib,debugging
- depuración de DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260575"
---
# <a name="timing-windows-multimedia"></a>Tiempo (Windows Multimedia)

Como parte de la depuración de una aplicación, puede obtener información sobre la cantidad de tiempo necesaria para completar operaciones DrawDib repetitivas. La [**función DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) devuelve información de tiempo para las operaciones siguientes:

-   Dibujar un mapa de bits
-   Descompresión de un mapa de bits
-   Dithering a bitmap
-   Ajustar un mapa de bits
-   Transferencia de un mapa de bits mediante [**la función BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Transferencia de un mapa de bits mediante [**la función StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

Después de recuperar un conjunto de valores, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) restablece el recuento y el valor de cada operación.

La [**función DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) solo está disponible en la versión de depuración de las funciones DrawDib.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de imágenes](image-rendering.md)
</dt> </dl>

 

 
