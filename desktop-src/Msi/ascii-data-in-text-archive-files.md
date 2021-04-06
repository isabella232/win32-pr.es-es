---
description: Cuando una tabla que solo contiene caracteres ASCII se exporta a un archivo de almacenamiento de texto, el archivo. IDT se ajusta al formato de archivo de almacenamiento básico.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Datos ASCII en archivos de almacenamiento de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909082"
---
# <a name="ascii-data-in-text-archive-files"></a>Datos ASCII en archivos de almacenamiento de texto

Cuando una tabla que solo contiene caracteres ASCII se exporta a un [archivo de almacenamiento de texto](text-archive-files.md), el archivo. IDT se ajusta al [formato de archivo de almacenamiento](archive-file-format.md)básico. Si la tabla contiene información que no es ASCII, el formato del archivo de almacenamiento se amplía para incluir información de la página de códigos.

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>Archivos de texto que contienen solo caracteres ASCII

Cuando una tabla que solo contiene caracteres ASCII se exporta a un archivo de almacenamiento, el archivo. IDT está en el [formato de archivo de almacenamiento](archive-file-format.md)básico. Cada secuencia de la tabla se exporta como un archivo con la extensión de nombre de archivo. ibd. Los archivos. ibd se almacenan en una carpeta con el mismo nombre que la tabla. Por ejemplo, considere la posibilidad de exportar la siguiente tabla [binaria](binary-table.md) .



| Nombre  | Datos      |
|-------|-----------|
| Libros | Books. ibd |
| Cars  | Cars. ibd  |



 

La estructura de directorios después de exportar esta tabla es la siguiente. La información de la tabla de la base de datos se exporta a Binary. IDT. Las dos secuencias de datos binarios se exportan a Book. ibd y Cars. ibd guardado en la carpeta denominada Binary.

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

El archivo de almacenamiento binario. IDT está en el [formato de archivo de almacenamiento](archive-file-format.md) básico y tendría el aspecto siguiente.

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>Archivos de texto que contienen caracteres que no son ASCII

Si el archivo contiene datos que no son ASCII, el [formato de archivo de almacenamiento](archive-file-format.md) básico del archivo. IDT se amplía para incluir información de la página de códigos. La tercera fila de la tabla. IDT es la página de códigos numérica seguida del nombre de tabla y los nombres de columna de clave principal separados por tabulaciones.

> [!Note]  
> Un archivo. IDT que contiene información no ASCII se debe guardar en formato ASCII. Por ejemplo, un archivo de almacenamiento de texto puede contener los nombres de tabla y columna codificados como UTF-8, pero el propio archivo de almacenamiento debe ser ASCII.

 

La siguiente tabla de ActionText localizada en francés incluiría información no ASCII. La página de códigos numérica utilizada para las cadenas en francés es 1252.



| Acción    | Descripción                                  | Plantilla |
|-----------|----------------------------------------------|----------|
| ANUNCIAR | Publicación d'informations sur l'application |          |



 

El archivo de almacenamiento exportado, ActionText. IDT, sería como se indica a continuación.

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> Si un archivo de almacenamiento de texto contiene datos que no son ASCII, el archivo de almacenamiento incluye información de la página de códigos. Los archivos de almacenamiento con información de página de códigos solo se pueden volver a importar en una base de datos de esa página de códigos exacta o en una base de datos independiente del lenguaje. En el caso de una base de datos independiente del lenguaje, la página de códigos se establece en la página de códigos del archivo de almacenamiento. Para obtener más información sobre cómo Windows Installer controla las páginas de códigos, vea la sección [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).

 

 

 



