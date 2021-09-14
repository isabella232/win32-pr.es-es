---
description: Dado que la copia innecesaria de archivos ralentiza una instalación, el instalador de Windows determina si el archivo de clave del componente ya está instalado antes de intentar instalar los archivos de cualquier componente.
ms.assetid: 8be734c7-4f16-4f54-93db-bb8efb1ea6da
title: Reemplazar archivos existentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b3908749e5496e4be9bf0ff68c7038a9ea6573
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274127"
---
# <a name="replacing-existing-files"></a>Reemplazar archivos existentes

Dado que la copia innecesaria de archivos ralentiza una instalación, el instalador de Windows determina si el archivo de clave del componente ya está instalado antes de intentar instalar los archivos de cualquier componente. Si el instalador encuentra un archivo con el mismo nombre que el archivo de clave del componente instalado en la ubicación de destino, compara la versión, la fecha y el idioma de los dos archivos clave y usa reglas de control de versiones de archivos para determinar si se debe instalar el componente proporcionado por el paquete. Si el instalador determina que debe reemplazar el componente en función del archivo de clave, usa las reglas de control de versiones de archivos en cada archivo instalado para determinar si se debe reemplazar el archivo.

Tenga en cuenta que al crear un paquete de instalación con [](file-table.md) archivos con versiones, la cadena de versión de la columna Versión de la tabla Archivo siempre debe ser idéntica a la versión del archivo incluido con el paquete.

Las reglas de control de versiones de archivos predeterminadas se pueden invalidar o modificar mediante la [**propiedad REINSTALLMODE.**](reinstallmode.md) El instalador usa las reglas de control de versiones de archivos especificadas por la **propiedad REINSTALLMODE** al instalar, reinstalar o reparar un archivo. En el ejemplo siguiente se muestra cómo el instalador aplica las reglas de control de [versiones de archivos predeterminadas.](file-versioning-rules.md) El valor predeterminado de la **propiedad REINSTALLMODE** es "omus".

Los siguientes archivos de clave de componente se instalan en el sistema antes de volver a instalar el componente.



| Archivo                                    | Versión  | Fecha de creación | Fecha de modificación | Idioma    |
|-----------------------------------------|----------|-------------|---------------|-------------|
| Archivo A                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileB                                   | 2.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileC                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| Presentado                                   | 1.0.0000 | 1/1/99      | 1/2/99        | ESN         |
| FileE                                   | ninguno     | 1/1/99      | 1/1/99        | ninguno        |
| FileF (modificado > crear)<br/> | ninguno     | 1/1/99      | 1/2/99        | ninguno        |
| FileG                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileH                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG,FRN,SPN |
| FileI                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG,FRN     |
| FileJ                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG,HAN,ITN |



 

Los siguientes archivos de clave de componente se incluyen en el paquete del instalador.



| Archivo                               | Versión  | Fecha de creación | Fecha de modificación | Idioma    |
|------------------------------------|----------|-------------|---------------|-------------|
| ArchivoA (marcado igual)<br/>     | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileB (versión anterior)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileC (versión posterior)<br/>   | 2.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileD (versión posterior)<br/>   | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| FileE (marcado igual)<br/>     | ninguno     | 1/1/99      | 1/1/99        | ninguno        |
| FileF (nuevo archivo)<br/>        | ninguno     | 1/3/99      | 1/3/99        | ninguno        |
| FileG (nuevo lenguaje)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (nuevo lenguaje)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | ITN, ENG, HAN |
| FileI (más idiomas)<br/>  | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (menos idiomas)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | GER         |



 

Los siguientes archivos de clave de componente permanecen en el sistema después de reinstalar el componente. El estado del archivo de clave determina el estado de cualquier otro archivo del componente.



| Archivo                | Versión  | Fecha de creación | Fecha de modificación | Idioma    |
|---------------------|----------|-------------|---------------|-------------|
| FileA (original)    | 1.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileB (original)    | 2.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileC (reemplazo) | 2.0.0000 | 1/1/99      | 1/1/99        | ESN         |
| FileD (reemplazo) | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| FileE (reemplazo) | ninguno     | 1/1/99      | 1/1/99        | ninguno        |
| FileF (original)    | ninguno     | 1/1/99      | 1/2/99        | ninguno        |
| FileG (reemplazo) | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (reemplazo) | 1.0.0000 | 1/1/99      | 1/1/99        | ITN, ENG, HAN |
| FileI (reemplazo) | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (original)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG,HAN,ITN |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comprobación de CRC durante una instalación](crc-checking-during-an-installation.md)
</dt> </dl>

 

 




