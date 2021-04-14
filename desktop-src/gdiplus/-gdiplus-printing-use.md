---
description: Con unos pocos ajustes secundarios en el código, puede enviar la salida GDI+ de Windows a una impresora en lugar de a una pantalla.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Imprimir (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985138"
---
# <a name="printing-gdi"></a>Imprimir (GDI+)

Con unos pocos ajustes secundarios en el código, puede enviar la salida GDI+ de Windows a una impresora en lugar de a una pantalla. Para dibujar en una impresora, obtenga un identificador de contexto de dispositivo para la impresora y pase ese identificador a un constructor [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Coloque los comandos de dibujo de GDI+ entre las llamadas a [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) y [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

En los temas siguientes se explica con más detalle el envío de salidas GDI+ a las impresoras:

-   [Envío de la salida de GDI+ a una impresora](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Mostrar un cuadro de diálogo de impresión](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Optimización de la impresión mediante el suministro de un identificador de impresora](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



