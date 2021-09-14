---
description: Cuando una tabla que contiene solo caracteres ASCII se exporta a un archivo de archivo de texto, el archivo .idt se adhiere al formato de archivo de archivo básico.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Datos ASCII en archivos de archivo de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159067"
---
# <a name="ascii-data-in-text-archive-files"></a>Datos ASCII en archivos de archivo de texto

Cuando una tabla que contiene solo caracteres ASCII se exporta [a](text-archive-files.md)un archivo de archivo de texto , el archivo .idt cumple el formato de archivo de [archivo básico](archive-file-format.md). Si la tabla contiene información que no es ASCII, el formato del archivo de archivo se amplía para incluir información de página de códigos.

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>Archivos de archivo de texto que solo contienen caracteres ASCII

Cuando una tabla que contiene solo caracteres ASCII se exporta a un archivo de archivo, el archivo .idt tiene el formato de archivo [de archivo básico](archive-file-format.md). Cada secuencia de la tabla se exporta como un archivo con una extensión de nombre de archivo .ibd. Los archivos .ibd se almacenan en una carpeta con el mismo nombre que la tabla. Por ejemplo, considere la exportación de la [siguiente tabla](binary-table.md) binaria.



| Nombre  | Datos      |
|-------|-----------|
| Libros | Books.ibd |
| Cars  | Cars.ibd  |



 

La estructura de directorios después de exportar esta tabla es la siguiente. La información de la tabla de base de datos se exporta a Binary.idt. Los dos flujos de datos binarios se exportan a Book.ibd y Cars.ibd guardados en la carpeta denominada Binary.

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

El archivo de archivo Binary.idt tiene el formato de archivo [de archivo](archive-file-format.md) básico y tendría el siguiente aspecto.

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>Archivos de archivo de texto que contienen caracteres que no son ASCII

Si el archivo contiene datos que [](archive-file-format.md) no son ASCII, el formato de archivo de archivo básico del archivo .idt se amplía para incluir información de la página de códigos. La tercera fila de la tabla .idt es la página de códigos numérica seguida del nombre de tabla y los nombres de columna de clave principal separados por pestañas.

> [!Note]  
> Un archivo .idt que contiene información no ASCII debe guardarse en formato ASCII. Por ejemplo, un archivo de archivo de texto puede contener los nombres de columna y tabla codificados como UTF-8, pero el propio archivo de archivo debe ser ASCII.

 

La siguiente tabla ActionText localizada en francés contendrá información que no es ASCII. La página de códigos numérica usada para las cadenas en francés es 1252.



| Acción    | Descripción                                  | Plantilla |
|-----------|----------------------------------------------|----------|
| ANUNCIAR | Publication d'informations sur l'application |          |



 

El archivo de archivo exportado, ActionText.idt, sería el siguiente.

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> Si un archivo de archivo de texto contiene datos que no son ASCII, el archivo de archivo incluye información de la página de códigos. Los archivos de archivo con información de página de códigos solo se pueden volver a importar en una base de datos de esa página de códigos exacta o en una base de datos neutra de idioma. En el caso de una base de datos con idioma neutro, la página de códigos se establece en la página de códigos del archivo de archivo. Para obtener más información sobre cómo el Windows controla las páginas de códigos, vea la sección Control de páginas de [códigos (Windows instalador).](code-page-handling-windows-installer-.md)

 

 

 



