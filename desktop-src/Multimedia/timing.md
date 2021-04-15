---
title: Temporización (Windows multimedia)
description: Control de tiempo
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, temporización
- DrawDibTime función)
- DrawDib, depuración
- depurar DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488753"
---
# <a name="timing-windows-multimedia"></a>Temporización (Windows multimedia)

Como parte de la depuración de una aplicación, puede obtener información sobre la cantidad de tiempo necesario para completar las operaciones repetitivas de DrawDib. La función [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) devuelve información de tiempo para las siguientes operaciones:

-   Dibujo de un mapa de bits
-   Descomprimir un mapa de bits
-   Tramar un mapa de bits
-   Ajustar un mapa de bits
-   Transferir un mapa de bits mediante la función [**bitblt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Transferir un mapa de bits mediante la función [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

Después de recuperar un conjunto de valores, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) restablece el recuento y el valor de cada operación.

La función [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) solo está disponible en la versión de depuración de las funciones DrawDib.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de imágenes](image-rendering.md)
</dt> </dl>

 

 
