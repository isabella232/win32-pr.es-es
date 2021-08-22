---
description: ICE39 valida el flujo de información de resumen de la base de datos.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb912afbe7220eee1aa3bbcd494f6531736279b85c5736f6867fdf8779e39bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528445"
---
# <a name="ice39"></a>ICE39

ICE39 valida el flujo [de información de resumen](summary-information-stream.md) de la base de datos.

ICE39 comprueba el formato de las siguientes propiedades:

-   [**Resumen del recuento de palabras**](word-count-summary.md)
-   [**Resumen del recuento de páginas**](page-count-summary.md)
-   [**Resumen de plantilla**](template-summary.md)
-   [**Resumen del número de revisión**](revision-number-summary.md)
-   [**Resumen de fecha y hora de creación**](create-time-date-summary.md)
-   [**Resumen de fecha y hora del último guardado**](last-saved-time-date-summary.md)
-   [**Resumen de la última impresión**](last-printed-summary.md)

Si la [**propiedad Resumen de recuento**](word-count-summary.md) de palabras especifica que el origen está comprimido, ICE39 envía una advertencia si los archivos también se marcan como comprimidos en la columna Atributos de la tabla [Archivo](file-table.md). Vea Using Cabinets and Compressed Sources (Uso de [gabinetes y orígenes comprimidos).](using-cabinets-and-compressed-sources.md)

ICE39 envía una advertencia si la propiedad [**Resumen**](word-count-summary.md) de recuento de palabras especifica que el paquete es compatible con UAC y que la tabla [MsiPackageCertificate](msipackagecertificate-table.md) no está vacía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



