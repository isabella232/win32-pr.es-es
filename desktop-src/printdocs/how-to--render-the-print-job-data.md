---
description: En este tema se describe cómo representar los datos del programa que se imprimirán.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Cómo: Representar datos del trabajo de impresión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70724cc9dee6b7d3bb0434f08e3db959acfecfc54bc4ebafac5f5a3c6bd4b014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825135"
---
# <a name="how-to-render-print-job-data"></a>Cómo: Representar datos del trabajo de impresión

En este tema se describe cómo representar los datos del programa que se imprimirán. En este tema no se explica en detalle cómo representar gráficos o imágenes de texto específicos. En su lugar, describe cómo administrar los datos del programa y representarlos como un documento XPS, que envía a una impresora mediante [xps Print API](xps-printing.md).

## <a name="overview"></a>Información general

La representación de datos del trabajo de impresión para la impresión implica tomar los datos específicos del programa, como texto, imágenes y formato, y convertirlos en un formato compatible con la impresora de destino. El programa que envía los datos a la impresora debe enviarlos en el formato que requiera el controlador de impresora.

Use [XPS Print API para](xps-printing.md) enviar los datos a la impresora y requiere que los datos se formatee como un documento XPS. Para generar el contenido del documento XPS que necesita la API de impresión XPS, el programa de ejemplo usa [la API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).

Si el contenido del programa está en un formato que no es compatible con una impresora, deberá representarse antes de que se envíe a la impresora. Si el programa usa la API de documentos [XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para administrar su contenido del programa, el contenido del programa estará en un formato que se puede enviar directamente a [xps Print API](xps-printing.md) y no requerirá ninguna representación adicional antes de enviarlo a la impresora.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[XPS Print API](xps-printing.md)
</dt> </dl>

 

 
