---
description: ICE60 valida la tabla de archivos de una base de datos Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667942"
---
# <a name="ice60"></a>ICE60

ICE60 comprueba que los archivos de la [tabla de archivos](file-table.md) cumplen la siguiente condición:

-   Si el archivo no es una fuente y tiene una versión, debe tener un idioma.
-   ICE60 comprueba que no hay ningún archivo con versión en la [tabla MsiFileHash](msifilehash-table.md).

Un error al corregir una advertencia de ICE60 suele conducir a que un archivo se reinstale innecesariamente cuando se realiza una reparación del producto. Esto sucede porque el archivo que se va a instalar en la reparación y el archivo existente en el disco tienen la misma versión (son el mismo archivo) pero distintos idiomas. La tabla de archivos muestra el idioma como null, pero el propio archivo tiene un valor de idioma en el recurso. En función de las [reglas de control de versiones de archivo](file-versioning-rules.md), el instalador favorece el archivo que se va a instalar, por lo que se Recopia innecesariamente.

## <a name="result"></a>Resultado

ICE60 envía una advertencia o un error si un archivo de la [tabla de archivos](file-table.md) que no es una fuente y tiene una versión, no tiene un idioma.

ICE60 envía el siguiente error si un archivo que aparece en la tabla MsiFileHash tiene versiones.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Ejemplo

ICE60 notifica el siguiente error y advertencia para el ejemplo que se muestra. (El archivo B es una fuente; los demás archivos no lo son).

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

Filea tiene una versión y un idioma; por lo tanto, no se genera ninguna advertencia o error.

FileB tiene una versión pero no un idioma. Sin embargo, no se genera ninguna advertencia ni error, porque es una fuente.

FileC es una referencia complementaria, por lo que no tiene que tener un idioma. No se genera ninguna advertencia o error.

Archivó no tiene ninguna versión, por lo que no necesita tener un idioma. No se genera ninguna advertencia o error.

El archivo tiene una versión pero no un idioma. Por lo tanto, se genera una advertencia.

Para corregir esta advertencia, agregue un idioma al archivo.

Los archivos deben tener valores de idioma almacenados en el recurso de versión siempre que sea posible. Si un archivo es independiente del idioma, use el [LANGID](column-data-types.md) 0.

[Tabla de archivos](file-table.md) (FileB es una fuente; los demás archivos no lo son).



| Archivo  | Versión | Idioma |
|-------|---------|----------|
| Archivoa | 1,0     | 3082     |
| FileB | 1,0     |          |
| FileC | Archivoa   |          |
| Registrado |         |          |
| Archivo | 1,0     |          |



 

[Tabla de fuentes](font-table.md)



| Archivo  | FontTitle  |
|-------|------------|
| FileB | Título de fuente |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



