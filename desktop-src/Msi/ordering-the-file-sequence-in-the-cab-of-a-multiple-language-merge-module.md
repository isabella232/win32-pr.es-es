---
description: Se deben crear módulos de combinación de varios idiomas, transformaciones de idioma y archivos de archivador para que el orden de los archivos coincida con el orden especificado en la tabla Archivo.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Ordenar la secuencia de archivos en la CAB de un módulo de combinación de varios lenguajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e0d7d5efc3c4599f7a3f0eecce2101d1a7db034be6e0f80eda30245a95204d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942812"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Ordenar la secuencia de archivos en la CAB de un módulo de combinación de varios lenguajes

Los módulos de combinación de varios idiomas, las transformaciones de idioma y los archivos de archivador deben crearse de forma que el orden de los archivos del .cab coincida con el orden de instalación de los archivos especificados en la tabla de archivos [,](file-table.md)incluso después de la aplicación de la transformación de idioma. Si el orden en el módulo y en el .cab no coinciden, no se puede usar el módulo de combinación.

Asigne a cada archivo del módulo, un número de secuencia único que sea independiente de su lenguaje y, a continuación, use siempre ese número de secuencia para el archivo. Use la misma secuencia al compilar el archivo de archivador y crear una transformación de lenguaje.

Dado que el instalador solo instala los archivos enumerados en la tabla de archivos [,](file-table.md)el uso de una secuencia de archivos global en el archivador, [](file-table.md)la tabla de archivos y la transformación de lenguaje permite a la herramienta de combinación omitir los archivos adicionales almacenados en el archivador que no aparecen en la tabla de [archivos](file-table.md). Puede haber otros archivos en el archivador, pero no deben aparecer en la [tabla de archivos](file-table.md). Por ejemplo, un módulo que instala Code.dll, English.dat, German.dat y French.dat puede usar el siguiente orden de secuencia de archivos global.



| Archivo        | Secuencia |
|-------------|----------|
| Code.Dll    | 1        |
| English.Dat | 2        |
| German.Dat  | 3        |
| French.Dat  | 4        |



 

A continuación, se pueden crear transformaciones de idioma para modificar la tabla [de archivos](file-table.md) del módulo para inglés, alemán o francés.

[Tabla de archivos](file-table.md) (parcial para inglés)



| Archivo        | Secuencia |
|-------------|----------|
| Code.Dll    | 1        |
| English.Dat | 2        |



 

[Tabla de archivos](file-table.md) (parcial para alemán)



| Archivo       | Secuencia |
|------------|----------|
| Code.Dll   | 1        |
| German.Dat | 3        |



 

[Tabla de archivos](file-table.md) (parcial para francés)



| Archivo       | Secuencia |
|------------|----------|
| Code.Dll   | 1        |
| French.Dat | 4        |



 

Para obtener más información, vea Crear una transformación de lenguaje para un módulo de combinación de varios [idiomas](authoring-a-language-transform-for-a-multiple-language-merge-module.md) y Crear tablas de archivo [de módulo de mezcla](authoring-merge-module-file-tables.md).

 

 



