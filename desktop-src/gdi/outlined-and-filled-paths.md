---
description: Una aplicación puede dibujar el contorno de una ruta de acceso mediante una llamada a la función StrokePath, que puede rellenar el interior de una ruta de acceso mediante una llamada a la función FillPath, y puede describir y rellenar la ruta de acceso mediante una llamada a la función StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Trazados contornos y rellenos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001520"
---
# <a name="outlined-and-filled-paths"></a>Trazados contornos y rellenos

Una aplicación puede dibujar el contorno de una ruta de acceso mediante una llamada a la función [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , que puede rellenar el interior de una ruta de acceso mediante una llamada a la función [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) , y puede describir y rellenar la ruta de acceso mediante una llamada a la función [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .

Cada vez que una aplicación rellena una ruta de acceso, el sistema utiliza el modo de relleno actual del controlador de dominio. Una aplicación puede recuperar este modo mediante una llamada a la función [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) , y puede establecer un nuevo modo de relleno mediante una llamada a la función [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . Para obtener una descripción de los dos modos de relleno, consulte [regiones](regions.md).

En la ilustración siguiente se muestra la sección transversal de un objeto creado por una aplicación de diseño asistido por PC (CAD) mediante rutas de acceso que se han esquematizado y rellenado.

![Ilustración que muestra la vista transversal de un objeto, con varias partes indicadas por diferentes patrones de relleno](images/cspth-01.png)

 

 



