---
description: En este tema se describe cómo representar los datos del programa que se van a imprimir.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Cómo: representar datos de trabajos de impresión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913150"
---
# <a name="how-to-render-print-job-data"></a>Cómo: representar datos de trabajos de impresión

En este tema se describe cómo representar los datos del programa que se van a imprimir. En este tema no se explica con detalle cómo representar gráficos o imágenes de texto específicos. En su lugar, se describe cómo administrar los datos del programa y representarlos como un documento XPS, que envía a una impresora mediante la [API de impresión XPS](xps-printing.md).

## <a name="overview"></a>Información general

La representación de datos del trabajo de impresión para la impresión implica tomar los datos específicos del programa, como texto, imágenes y formato, y convertirlos a un formato compatible con la impresora de destino. El programa que envía los datos a la impresora debe enviarlos en el formato que requiera el controlador de impresora.

Use la [API de impresión XPS](xps-printing.md) para enviar los datos a la impresora y requiere que los datos estén formateados como un documento XPS. Para generar el contenido del documento XPS que necesita la API de impresión XPS, el programa de ejemplo usa la [API de documentos XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).

Si el contenido del programa está en un formato que no es compatible con una impresora, deberá representarse antes de que se envíe a la impresora. Si el programa usa la [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para administrar el contenido del programa, el contenido del programa estará en un formato que se pueda enviar directamente a la [API de impresión XPS](xps-printing.md) y no requerirá ninguna representación adicional antes de enviarlo a la impresora.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API de impresión XPS](xps-printing.md)
</dt> </dl>

 

 
