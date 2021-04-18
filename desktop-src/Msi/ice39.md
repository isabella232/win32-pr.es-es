---
description: ICE39 valida la secuencia de información de Resumen de la base de datos.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652815"
---
# <a name="ice39"></a>ICE39

ICE39 valida la [secuencia de información de Resumen](summary-information-stream.md) de la base de datos.

ICE39 comprueba el formato de las siguientes propiedades:

-   [**Resumen de recuento de palabras**](word-count-summary.md)
-   [**Resumen de recuento de páginas**](page-count-summary.md)
-   [**Resumen de plantillas**](template-summary.md)
-   [**Resumen de número de revisión**](revision-number-summary.md)
-   [**Crear Resumen de fecha y hora**](create-time-date-summary.md)
-   [**Resumen de fecha y hora de la última vez que se guardó**](last-saved-time-date-summary.md)
-   [**Último resumen impreso**](last-printed-summary.md)

Si la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) especifica que el origen está comprimido, ICE39 publica una advertencia si algún archivo también está marcado como comprimido en la columna atributos de la [tabla de archivos](file-table.md). Consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).

ICE39 publica una advertencia si la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) especifica que el paquete es compatible con UAC y que la [tabla MsiPackageCertificate](msipackagecertificate-table.md) no está vacía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



