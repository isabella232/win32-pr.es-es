---
description: Con algunos ajustes menores en el código, puede enviar Windows GDI+ salida a una impresora en lugar de a una pantalla.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Impresión (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5807c976ef3224bc4b66afc0bb8637d79d725f12cbdebd3199d9710ae529a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885086"
---
# <a name="printing-gdi"></a>Impresión (GDI+)

Con algunos ajustes menores en el código, puede enviar Windows GDI+ salida a una impresora en lugar de a una pantalla. Para dibujar en una impresora, obtenga un identificador de contexto de dispositivo para la impresora y pase ese identificador a un constructor [**Gráfico.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Coloque el GDI+ comandos de dibujo entre llamadas [a StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) y [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

En los temas siguientes se trata el envío GDI+ salida a impresoras con más detalle:

-   [Envío de la salida de GDI+ a una impresora](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Mostrar un cuadro de diálogo Imprimir](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Optimización de la impresión mediante el suministro de un identificador de impresora](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



