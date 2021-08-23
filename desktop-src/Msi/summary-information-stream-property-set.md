---
description: En la tabla siguiente se muestra el conjunto de propiedades de flujo de información de resumen, que incluye las propiedades, sus correspondientes iDs de propiedad, PID y tipos.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Conjunto de propiedades de flujo de información de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d41439e15a59ca1942fcbb49c06067251060935b165d6a34972df868fa7feac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627055"
---
# <a name="summary-information-stream-property-set"></a>Conjunto de propiedades de flujo de información de resumen

En la tabla siguiente se muestra el conjunto de propiedades de flujo de información de resumen, que incluye las propiedades, sus correspondientes iDs de propiedad, PID y tipos. Para obtener más información sobre cómo el instalador usa estas propiedades, vea [Resumen de descripciones de propiedades](summary-property-descriptions.md). Para obtener información sobre las funciones del Instalador de ventana que se usan para configurar las propiedades de información de resumen, vea [Using the Summary Information Stream](using-the-summary-information-stream.md).



| Nombre de propiedad                                                | Id. de propiedad        | PID | Tipo         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**Codepage**](codepage-summary.md)                         | PÁGINA \_ DE CÓDIGOS PID      | 1   | VT \_ I2       |
| [**Título**](title-summary.md)                               | TÍTULO \_ DE PID         | 2   | VT \_ LPSTR    |
| [**Asunto**](subject-summary.md)                           | ASUNTO DEL \_ PID       | 3   | VT \_ LPSTR    |
| [**Autor**](author-summary.md)                             | AUTOR DE \_ PID        | 4   | VT \_ LPSTR    |
| [**Palabras clave**](keywords-summary.md)                         | PALABRAS \_ CLAVE PID      | 5   | VT \_ LPSTR    |
| [**Comentarios**](comments-summary.md)                         | COMENTARIOS \_ DE PID      | 6   | VT \_ LPSTR    |
| [**Plantilla**](template-summary.md)                         | PLANTILLA \_ DE PID      | 7   | VT \_ LPSTR    |
| [**Guardado por última vez por**](last-saved-by-summary.md)               | PID \_ LASTAUTHOR    | 8   | VT \_ LPSTR    |
| [**Número de revisión**](revision-number-summary.md)           | PID \_ REVNUMBER     | 9   | VT \_ LPSTR    |
| [**Última impresión**](last-printed-summary.md)                 | PID \_ LASTPRINTED   | 11  | VT \_ FILETIME |
| [**Fecha y hora de creación**](create-time-date-summary.md)         | PID \_ CREATE \_ DTM   | 12  | VT \_ FILETIME |
| [**Hora y fecha de último guardado**](last-saved-time-date-summary.md)  | PID \_ LASTSAVE \_ DTM | 13  | VT \_ FILETIME |
| [**Recuento de páginas**](page-count-summary.md)                     | PID \_ PAGECOUNT     | 14  | VT \_ I4       |
| [**Recuento de palabras**](word-count-summary.md)                     | PID \_ WORDCOUNT     | 15  | VT \_ I4       |
| [**Recuento de caracteres**](character-count-summary.md)           | PID \_ CHARCOUNT     | 16  | VT \_ I4       |
| [**Creación de una aplicación**](creating-application-summary.md) | PID \_ APPNAME       | 18  | VT \_ LPSTR    |
| [**Seguridad**](security-summary.md)                         | SEGURIDAD DE \_ PID      | 19  | VT \_ I4       |



 

Actualmente, el instalador mantiene tres formatos de almacenamiento para paquetes de instalación, transformaciones y paquetes de revisión. El CLSID del almacenamiento se establece en la clase de formato adecuada para el formato determinado, independientemente de la información de resumen del almacenamiento.

 

 



