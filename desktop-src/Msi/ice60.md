---
description: ICE60 valida la tabla File de una base de Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8d2cbf9136ea6195a138c586d4408dc0d2e5ff411b52fd73fec8a569c5d186
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044035"
---
# <a name="ice60"></a>ICE60

ICE60 comprueba que los archivos de la [tabla File](file-table.md) cumplen la condición siguiente:

-   Si el archivo no es una fuente y tiene una versión, debe tener un idioma.
-   ICE60 comprueba que no se muestran archivos con control de versiones en la [tabla MsiFileHash](msifilehash-table.md).

Si no se corrige una advertencia notificada por ICE60, normalmente se vuelve a instalar un archivo cuando se realiza una reparación del producto. Esto sucede porque el archivo que se va a instalar en la reparación y el archivo existente en el disco tienen la misma versión (son el mismo archivo), pero idiomas diferentes. En la tabla de archivos se muestra el idioma como NULL, pero el propio archivo tiene un valor de idioma en el recurso. En función de [las reglas de control](file-versioning-rules.md)de versiones de archivo, el instalador prefiere que el archivo se instale, por lo que se vuelve a copiar sin necesidad.

## <a name="result"></a>Resultado

ICE60 envía una advertencia o un [](file-table.md) error si un archivo de la tabla File que no es una fuente y tiene una versión, no tiene un idioma.

ICE60 publica el siguiente error si se ha versionado un archivo enumerado en la tabla MsiFileHash.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Ejemplo

ICE60 notifica el siguiente error y advertencia para el ejemplo mostrado. (El archivo B es una fuente; los demás archivos no).

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

FileA tiene una versión y un lenguaje; por lo tanto, no se genera ninguna advertencia o error.

FileB tiene una versión, pero no un lenguaje. Sin embargo, no se genera ninguna advertencia o error porque es una fuente.

FileC es una referencia complementaria, por lo que no tiene que tener un idioma. No se genera ninguna advertencia o error.

FileD no tiene ninguna versión, por lo que no necesita tener un idioma. No se genera ninguna advertencia o error.

FileE tiene una versión, pero no un idioma. Por lo tanto, se genera una advertencia.

Para corregir esta advertencia, agregue un idioma a FileE.

Los archivos deben tener valores de idioma almacenados en el recurso de versión siempre que sea posible. Si un archivo es neutral en el idioma, use [LANGID](column-data-types.md) 0.

[Tabla de](file-table.md) archivos (FileB es una fuente; los demás archivos no).



| Archivo  | Versión | Lenguaje |
|-------|---------|----------|
| ArchivoA | 1.0     | 3082     |
| FileB | 1.0     |          |
| FileC | ArchivoA   |          |
| Presentado |         |          |
| FileE | 1.0     |          |



 

[Tabla de fuentes](font-table.md)



| Archivo  | FontTitle  |
|-------|------------|
| FileB | Título de fuente |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



