---
description: Dado que la copia de archivos innecesarios ralentiza una instalación, el Windows Installer determina si el archivo de clave del componente ya está instalado antes de intentar instalar los archivos de cualquier componente.
ms.assetid: 8be734c7-4f16-4f54-93db-bb8efb1ea6da
title: Reemplazar archivos existentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b3908749e5496e4be9bf0ff68c7038a9ea6573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910690"
---
# <a name="replacing-existing-files"></a>Reemplazar archivos existentes

Dado que la copia de archivos innecesarios ralentiza una instalación, el Windows Installer determina si el archivo de clave del componente ya está instalado antes de intentar instalar los archivos de cualquier componente. Si el instalador encuentra un archivo con el mismo nombre que el archivo de clave del componente instalado en la ubicación de destino, compara la versión, la fecha y el idioma de los dos archivos de clave y utiliza reglas de control de versiones de archivo para determinar si se debe instalar el componente proporcionado por el paquete. Si el instalador determina que debe reemplazar la base del componente en el archivo de clave, utiliza las reglas de control de versiones de archivo en cada archivo instalado para determinar si se debe reemplazar el archivo.

Tenga en cuenta que al crear un paquete de instalación con archivos con versiones, la cadena de versión en la columna versión de la [tabla de archivos](file-table.md) siempre debe ser idéntica a la versión del archivo incluido con el paquete.

Las reglas de control de versiones de archivo predeterminadas se pueden reemplazar o modificar mediante la propiedad [**REINSTALLMODE**](reinstallmode.md) . El instalador utiliza las reglas de control de versiones de archivo especificadas por la propiedad **REINSTALLMODE** al instalar, reinstalar o reparar un archivo. En el ejemplo siguiente se muestra cómo el instalador aplica las [reglas de control de versiones de archivo](file-versioning-rules.md)predeterminadas. El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".

Los siguientes archivos de clave de componentes se instalan en el sistema antes de volver a instalar el componente.



| Archivo                                    | Versión  | Fecha de creación | Fecha de modificación | Idioma    |
|-----------------------------------------|----------|-------------|---------------|-------------|
| Archivoa                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileB                                   | 2.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileC                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| Registrado                                   | 1.0.0000 | 1/1/99      | 1/2/99        | ESN         |
| Archivo                                   | ninguno     | 1/1/99      | 1/1/99        | ninguno        |
| FileF (modificado > crear)<br/> | ninguno     | 1/1/99      | 1/2/99        | ninguno        |
| FileG                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileH                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| Archivo                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN     |
| FileJ                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, ALEMÁN, EN |



 

Los siguientes archivos de clave de componente se incluyen en el paquete del instalador.



| Archivo                               | Versión  | Fecha de creación | Fecha de modificación | Idioma    |
|------------------------------------|----------|-------------|---------------|-------------|
| Archivoa (marcado como el mismo)<br/>     | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileB (versión anterior)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileC (versión posterior)<br/>   | 2.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| Archivado (versión posterior)<br/>   | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| Archivo (marcado como el mismo)<br/>     | ninguno     | 1/1/99      | 1/1/99        | ninguno        |
| FileF (nuevo archivo)<br/>        | ninguno     | 1/3/99      | 1/3/99        | ninguno        |
| FileG (nuevo idioma)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (nuevo idioma)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | EN, ENG, ALEMÁN |
| Archivo (más idiomas)<br/>  | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (menos idiomas)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | ALEMÁN         |



 

Los siguientes archivos de clave de componente permanecen en el sistema después de reinstalar el componente. El estado del archivo de clave determina el estado de otros archivos del componente.



| Archivo                | Versión  | Fecha de creación | Fecha de modificación | Idioma    |
|---------------------|----------|-------------|---------------|-------------|
| Archivoa (original)    | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileB (original)    | 2.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileC (reemplazo) | 2.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| Archivado (reemplazo) | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| Archivo (reemplazo) | ninguno     | 1/1/99      | 1/1/99        | ninguno        |
| FileF (original)    | ninguno     | 1/1/99      | 1/2/99        | ninguno        |
| FileG (reemplazo) | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (reemplazo) | 1.0.0000 | 1/1/99      | 1/1/99        | EN, ENG, ALEMÁN |
| Archivo (reemplazo) | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (original)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, ALEMÁN, EN |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comprobación de CRC durante una instalación](crc-checking-during-an-installation.md)
</dt> </dl>

 

 




