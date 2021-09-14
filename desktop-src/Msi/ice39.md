---
description: ICE39 valida el flujo de información de resumen de la base de datos.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074612"
---
# <a name="ice39"></a>ICE39

ICE39 valida el [flujo de información de resumen de](summary-information-stream.md) la base de datos.

ICE39 comprueba el formato de las siguientes propiedades:

-   [**Resumen de recuento de palabras**](word-count-summary.md)
-   [**Resumen del recuento de páginas**](page-count-summary.md)
-   [**Resumen de plantillas**](template-summary.md)
-   [**Resumen del número de revisión**](revision-number-summary.md)
-   [**Resumen de fecha y hora de creación**](create-time-date-summary.md)
-   [**Resumen de fecha y hora guardadas por última vez**](last-saved-time-date-summary.md)
-   [**Último resumen impreso**](last-printed-summary.md)

Si la [**propiedad Resumen de recuento**](word-count-summary.md) de palabras especifica que el origen está comprimido, ICE39 envía una advertencia si los archivos también están marcados como comprimidos en la columna Atributos de la tabla [Archivo](file-table.md). Vea Using Cabinets and Compressed Sources ( Uso de [gabinetes y orígenes comprimidos).](using-cabinets-and-compressed-sources.md)

ICE39 envía una advertencia si la propiedad [**Resumen**](word-count-summary.md) de recuento de palabras especifica que el paquete es compatible con UAC y la tabla [MsiPackageCertificate](msipackagecertificate-table.md) no está vacía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



