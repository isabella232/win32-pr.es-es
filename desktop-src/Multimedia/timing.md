---
title: Control de tiempo (Windows Multimedia)
description: Control de tiempo
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib,timing
- Función DrawDibTime
- DrawDib,debugging
- depurar DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372535"
---
# <a name="timing-windows-multimedia"></a>Control de tiempo (Windows Multimedia)

Como parte de la depuración de una aplicación, puede obtener información sobre la cantidad de tiempo necesaria para completar operaciones drawDib repetitivas. La [**función DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) devuelve información de control de tiempo para las siguientes operaciones:

-   Dibujar un mapa de bits
-   Descompresión de un mapa de bits
-   Dithering a bitmap (Tramar un mapa de bits)
-   Ajustar un mapa de bits
-   Transferencia de un mapa de bits mediante la [**función BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Transferencia de un mapa de bits mediante [**la función StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

Después de recuperar un conjunto de valores, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) restablece el recuento y el valor de cada operación.

La [**función DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) solo está disponible en la versión de depuración de las funciones DrawDib.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de imágenes](image-rendering.md)
</dt> </dl>

 

 
