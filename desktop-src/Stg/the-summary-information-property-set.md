---
title: Conjunto de propiedades Demmary Information
description: COM define un conjunto de propiedades comunes estándar para almacenar información de resumen sobre documentos.
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54f942d0c7f6c7d1ebc37feda80d55420ea6c8aaf896f4df15df2a5b7e7c0ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886831"
---
# <a name="the-summary-information-property-set"></a>Conjunto de propiedades Demmary Information

COM define un conjunto de propiedades comunes estándar para almacenar información de resumen sobre documentos. El conjunto de propiedades Información de resumen debe almacenarse en un objeto de secuencia. Es decir, este conjunto de propiedades debe almacenarse como un conjunto de propiedades simple. Para obtener más información, [vea Storage y Objetos de secuencia para un conjunto de propiedades](storage-vs--stream-for-a-property-set.md).

Por ejemplo, para crear un conjunto de propiedades simple ANSI, llamaría a [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) para crear el conjunto de propiedades, especificando **PROPSETFLAG \_ ANSI** (simple es el tipo predeterminado del conjunto de propiedades) y, a continuación, escribiría en él con una llamada a [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Para leer el conjunto de propiedades, llamaría a [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple).

Todos los conjuntos de propiedades compartidas se identifican mediante un nombre de flujo o almacenamiento con el prefijo \\ "005" (o 0x05) para mostrar que se trata de un conjunto de propiedades que se puede compartir entre las aplicaciones. El conjunto de propiedades Información de resumen no es una excepción. El nombre de la secuencia que contiene el conjunto de propiedades Información de resumen es: **\\ "005SummaryInformation"**

No es necesario conocer el nombre de secuencia de la propiedad establecida al acceder a ella mediante los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de la [**interfaz IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) En este caso, solo es necesario conocer el identificador de formato (FMTID). El FMTID del conjunto de propiedades Información de resumen es: **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

La declaración de este valor está disponible en el archivo de encabezado como **FMTID \_ SummaryInformation**. Para obtener más información, vea FMTIDS en [Predefined Property Set Format Identifiers](predefined-property-set-format-identifiers.md).

En la tabla siguiente se enumeran los nombres de propiedad de cadena para el conjunto de propiedades Información de resumen, junto con los identificadores de propiedad respectivos y los indicadores de tipo variable (VT). Los nombres no se almacenan normalmente en el conjunto de propiedades, pero se deducen del valor de Id. de propiedad. Las entradas de cadena de id. de propiedad que se muestran aquí corresponden a las definiciones que se encuentran en los archivos de encabezado.

| Nombre | Cadena de identificador de propiedad | Id. de propiedad | Tipo VT |
|------|--------------------|-------------|---------|
| Título | PIDSI \_ TITLE | 0x00000002 | VT \_ LPSTR  |
| Asunto | ASUNTO \_ PIDSI | 0x00000003 | VT \_ LPSTR |
| Autor | PIDSI \_ AUTHOR | 0x00000004 | VT \_ LPSTR |
| Palabras clave | PALABRAS CLAVE \_ PIDSI | 0x00000005 | VT \_ LPSTR |
| Comentarios | COMENTARIOS \_ PIDSI | 0x00000006 | VT \_ LPSTR |
| Plantilla | PLANTILLA \_ PIDSI | 0x00000007 | VT \_ LPSTR |
| Guardado por última vez por | PIDSI \_ LASTAUTHOR | 0x00000008 | VT \_ LPSTR |
| Revision Number | PIDSI \_ REVNUMBER | 0x00000009 | VT \_ LPSTR |
| Tiempo total de edición | PIDSI \_ EDITTIME | 0x0000000A | VT \_ FILETIME (UTC) |
| Última impresión | PIDSI \_ LASTPRINTED | 0x0000000B | VT \_ FILETIME (UTC) |
| Fecha y hora de creación (consulte la nota siguiente) | PIDSI \_ CREATE \_ DTM | 0x0000000C | VT \_ FILETIME (UTC) |
| Hora/fecha guardadas por última vez (consulte la nota siguiente) | PIDSI \_ LASTSAVE \_ DTM | 0x0000000D | VT \_ FILETIME (UTC) |
| Número de páginas | PIDSI \_ PAGECOUNT | 0x0000000E | VT \_ I4 |
| Número de palabras | PIDSI \_ WORDCOUNT | 0x0000000F | VT \_ I4 |
| Número de caracteres | PIDSI \_ CHARCOUNT | 0x00000010 | VT \_ I4 |
| Miniatura | MINIATURA \_ DE PIDSI | 0x00000011 | VT \_ CF |
| Nombre de la creación de la aplicación | PIDSI \_ APPNAME | 0x00000012 | VT \_ LPSTR |
| Seguridad | SEGURIDAD \_ DE PIDSI | 0x00000013 | VT \_ I4 |

> [!NOTE]
> Para **Create Time/Date** y **Last saved Time/Date**, algunos métodos de transferencia de archivos, como una descarga de un BBS, no mantienen la versión del sistema de archivos de esta información correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementar el conjunto de propiedades Demmary Information](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




