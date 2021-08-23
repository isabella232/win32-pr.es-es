---
title: Control de tiempo (Windows Multimedia)
description: Control de tiempo
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib,timing
- Función DrawDibTime
- DrawDib,debugging
- depuración de DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc4324de5336a00b246ad644794ce8d0b3491bb644f34e8fc22dc8a7e460ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688085"
---
# <a name="timing-windows-multimedia"></a>Control de tiempo (Windows Multimedia)

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

 

 
