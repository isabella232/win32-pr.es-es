---
description: En la tabla siguiente se muestra el conjunto de propiedades de flujo de información de Resumen, que incluye las propiedades, sus identificadores de propiedad, PID y tipos correspondientes.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Conjunto de propiedades de flujo de información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3929e4180a85a8f154c0a0352ddd1f9a052769ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678588"
---
# <a name="summary-information-stream-property-set"></a>Conjunto de propiedades de flujo de información de Resumen

En la tabla siguiente se muestra el conjunto de propiedades de flujo de información de Resumen, que incluye las propiedades, sus identificadores de propiedad, PID y tipos correspondientes. Para obtener más información sobre cómo el instalador utiliza estas propiedades, vea [descripciones de propiedades de Resumen](summary-property-descriptions.md). Para obtener información sobre las funciones del instalador de Windows que se usan para configurar las propiedades de información de Resumen, vea [usar el flujo de información de Resumen](using-the-summary-information-stream.md).



| Nombre de propiedad                                                | Id. de propiedad        | PID | Tipo         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**737**](codepage-summary.md)                         | Página de códigos de PID \_      | 1   | I2 de VT \_       |
| [**Title**](title-summary.md)                               | Título del PID \_         | 2   | VT \_ LPSTR    |
| [**Asunto**](subject-summary.md)                           | asunto del PID \_       | 3   | VT \_ LPSTR    |
| [**Autor**](author-summary.md)                             | autor del PID \_        | 4   | VT \_ LPSTR    |
| [**Palabras clave**](keywords-summary.md)                         | \_palabras clave de PID      | 5   | VT \_ LPSTR    |
| [**Comentarios**](comments-summary.md)                         | Comentarios de PID \_      | 6   | VT \_ LPSTR    |
| [**Plantilla**](template-summary.md)                         | plantilla de PID \_      | 7   | VT \_ LPSTR    |
| [**Guardado por última vez por**](last-saved-by-summary.md)               | PID \_ LASTAUTHOR    | 8   | VT \_ LPSTR    |
| [**Número de revisión**](revision-number-summary.md)           | PID \_ REVNUMBER     | 9   | VT \_ LPSTR    |
| [**Última impresión**](last-printed-summary.md)                 | PID \_ LASTPRINTED   | 11  | VT \_ FILETIME |
| [**Crear hora/fecha**](create-time-date-summary.md)         | PID \_ Create \_ DTM   | 12  | VT \_ FILETIME |
| [**Fecha y hora de la última guardado**](last-saved-time-date-summary.md)  | PID \_ LASTSAVE \_ DTM | 13  | VT \_ FILETIME |
| [**Recuento de páginas**](page-count-summary.md)                     | PID \_ PAGECOUNT     | 14  | VT \_ I4       |
| [**Recuento de palabras**](word-count-summary.md)                     | PID \_ WORDCOUNT     | 15  | VT \_ I4       |
| [**Recuento de caracteres**](character-count-summary.md)           | CHARCOUNT de PID \_     | 16  | VT \_ I4       |
| [**Creando aplicación**](creating-application-summary.md) | PID \_ APPNAME       | 18  | VT \_ LPSTR    |
| [**Seguridad**](security-summary.md)                         | seguridad de PID \_      | 19  | VT \_ I4       |



 

El instalador mantiene actualmente tres formatos de almacenamiento para paquetes de instalación, transformaciones y paquetes de revisión. El CLSID para el almacenamiento se establece en la clase de formato adecuada para el formato determinado, independientemente de la información de resumen del almacenamiento.

 

 



