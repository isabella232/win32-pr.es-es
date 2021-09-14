---
description: Con algunos ajustes menores en el código, puede enviar Windows GDI+ salida a una impresora en lugar de a una pantalla.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Impresión (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063426"
---
# <a name="printing-gdi"></a>Impresión (GDI+)

Con algunos ajustes menores en el código, puede enviar Windows GDI+ salida a una impresora en lugar de a una pantalla. Para dibujar en una impresora, obtenga un identificador de contexto de dispositivo para la impresora y pase ese identificador a un constructor [**gráfico.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Coloque los GDI+ comandos de dibujo entre llamadas [a StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) y [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

En los temas siguientes se trata el envío GDI+ salida a las impresoras con más detalle:

-   [Envío de la salida de GDI+ a una impresora](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Mostrar un cuadro de diálogo Imprimir](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Optimización de la impresión mediante el suministro de un identificador de impresora](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



