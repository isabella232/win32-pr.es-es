---
description: Una aplicación puede dibujar el esquema de una ruta de acceso llamando a la función StrokePath, puede rellenar el interior de una ruta llamando a la función FillPath y puede describir y rellenar la ruta llamando a la función StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Rutas de acceso esquemateadas y rellenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660221eb1ef9d7ecf80d1d48ae18c8b234e76e5af3b30dba3323ee6feac3bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831605"
---
# <a name="outlined-and-filled-paths"></a>Rutas de acceso esquemateadas y rellenadas

Una aplicación puede dibujar el esquema de una ruta de acceso llamando a la función [**StrokePath,**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) puede rellenar el interior de una ruta llamando a la función [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) y puede describir y rellenar la ruta llamando a la función [**StrokeAndFillPath.**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath)

Cada vez que una aplicación rellena una ruta de acceso, el sistema usa el modo de relleno actual del controlador de dominio. Una aplicación puede recuperar este modo llamando a la función [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) y puede establecer un nuevo modo de relleno llamando a la [**función SetPolyFillMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) Para obtener una descripción de los dos modos de relleno, vea [Regiones](regions.md).

En la ilustración siguiente se muestra la sección cruzada de un objeto creado por una aplicación de diseño asistido por pc (CAD) mediante rutas de acceso que se han descrito y rellenado.

![ilustración que muestra la vista transversal de un objeto, con varias partes indicadas por patrones de relleno diferentes](images/cspth-01.png)

 

 



