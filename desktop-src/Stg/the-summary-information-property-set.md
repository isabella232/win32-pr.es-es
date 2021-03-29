---
title: Conjunto de propiedades de información de Resumen
description: COM define un conjunto de propiedades comunes estándar para almacenar información de resumen sobre documentos.
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb318daba7e0ad03ff176853877fe416ddeda799
ms.sourcegitcommit: fc240ac77d4c40a9f3a27714d7b852abbd234774
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/12/2019
ms.locfileid: "104419228"
---
# <a name="the-summary-information-property-set"></a>Conjunto de propiedades de información de Resumen

COM define un conjunto de propiedades comunes estándar para almacenar información de resumen sobre documentos. El conjunto de propiedades de información de resumen debe almacenarse en un objeto de secuencia. Es decir, este conjunto de propiedades debe almacenarse como un conjunto de propiedades simple. Para obtener más información, consulte [almacenamiento y objetos de secuencia para un conjunto de propiedades](storage-vs--stream-for-a-property-set.md).

Por ejemplo, para crear un conjunto de propiedades simples ANSI, llamaría a [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) para crear el conjunto de propiedades, especificando **PROPSETFLAG \_ ANSI** (simple es el tipo predeterminado de conjunto de propiedades) y, después, escribiría en él con una llamada a [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Para leer el conjunto de propiedades, llamaría a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple).

Todos los conjuntos de propiedades compartidas se identifican mediante un nombre de flujo o de almacenamiento con el prefijo " \\ 005" (o 0x05) para mostrar que es un conjunto de propiedades que se puede compartir entre aplicaciones. El conjunto de propiedades de información de resumen no es una excepción. El nombre de la secuencia que contiene el conjunto de propiedades de información de resumen es: **" \\ 005SummaryInformation"** .

No es necesario conocer el nombre de flujo del conjunto de propiedades cuando se tiene acceso a él por medio de los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . en este caso, solo es necesario conocer el identificador de formato (FMTID). El valor de FMTID para el conjunto de propiedades de información de resumen es: **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

La declaración para este valor está disponible en el archivo de encabezado como **FMTID \_ SummaryInformation**. Para obtener más información, vea FMTIDS en la [propiedad predefinida SET FORMAT Identifiers](predefined-property-set-format-identifiers.md).

En la tabla siguiente se enumeran los nombres de propiedad de cadena para el conjunto de propiedades de información de Resumen, junto con los identificadores de propiedad y los indicadores de tipo variable (VT) respectivos. Los nombres normalmente no se almacenan en el conjunto de propiedades, pero se deducen a partir del valor del identificador de propiedad. Las entradas de cadena de identificador de propiedad que se muestran aquí se corresponden con las definiciones que se encuentran en los archivos de encabezado.

| Nombre | Cadena de identificador de propiedad | Id. de propiedad | Tipo VT |
|------|--------------------|-------------|---------|
| Title | título de PIDSI \_ | 0x00000002 | VT \_ LPSTR  |
| Asunto | \_asunto PIDSI | 0x00000003 | VT \_ LPSTR |
| Autor | autor de PIDSI \_ | 0x00000004 | VT \_ LPSTR |
| Palabras clave | \_palabras clave de PIDSI | 0x00000005 | VT \_ LPSTR |
| Comentarios | Comentarios de PIDSI \_ | 0x00000006 | VT \_ LPSTR |
| Plantilla | \_plantilla PIDSI | 0x00000007 | VT \_ LPSTR |
| Guardado por última vez por | PIDSI \_ LASTAUTHOR | 0x00000008 | VT \_ LPSTR |
| Revision Number | PIDSI \_ REVNUMBER | 0x00000009 | VT \_ LPSTR |
| Tiempo total de edición | PIDSI \_ EDITTIME | 0x0000000A | VT \_ FILETIME (UTC) |
| Última impresión | PIDSI \_ LASTPRINTED | 0x0000000B | VT \_ FILETIME (UTC) |
| Fecha y hora de creación (vea la nota siguiente) | PIDSI \_ crear \_ DTM | 0x0000000C | VT \_ FILETIME (UTC) |
| Fecha y hora de la última vez que se guardó (vea la nota siguiente) | PIDSI \_ LASTSAVE \_ DTM | 0x0000000D | VT \_ FILETIME (UTC) |
| Número de páginas | PIDSI \_ PAGECOUNT | 0x0000000E | VT \_ I4 |
| Número de palabras | PIDSI \_ WORDCOUNT | 0x0000000F | VT \_ I4 |
| Número de caracteres | \_CHARCOUNT PIDSI | 0x00000010 | VT \_ I4 |
| Miniatura | miniatura de PIDSI \_ | 0x00000011 | VT \_ CF |
| Nombre de la creación de la aplicación | PIDSI \_ APPNAME | 0x00000012 | VT \_ LPSTR |
| Seguridad | seguridad de PIDSI \_ | 0x00000013 | VT \_ I4 |

> [!NOTE]
> En el caso de la fecha y hora de **creación** y la fecha y hora de la última vez que se **han guardado**, algunos métodos de transferencia de archivos, como una descarga de un BBS, no mantienen correctamente la versión del sistema de archivos de esta información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementar el conjunto de propiedades de información de Resumen](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




