---
description: Los módulos de combinación de varios idiomas, las transformaciones de idioma y los archivos. cab deben crearse de modo que el orden de los archivos coincida con el orden especificado en la tabla de archivos.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Ordenar la secuencia de archivos en el archivo. CAB de un módulo de combinación de varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279335"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Ordenar la secuencia de archivos en el archivo. CAB de un módulo de combinación de varios idiomas

Los módulos de combinación de varios idiomas, las transformaciones de lenguaje y los archivos. cab deben crearse de modo que el orden de los archivos del archivo. cab coincida con el orden de instalación de los archivos especificados en la [tabla de archivos](file-table.md), incluso después de la aplicación de la transformación de lenguaje. Si el orden en el módulo y en el archivo. cab no coinciden, no se puede usar el módulo de combinación.

Asigne a cada archivo del módulo un número de secuencia único que sea independiente del idioma y, a continuación, use siempre ese número de secuencia para el archivo. Use la misma secuencia al compilar el archivo. cab y crear una transformación de idioma.

Dado que el instalador solo instala los archivos enumerados en la [tabla de archivos](file-table.md), el uso de una secuencia de archivos global en el archivo. cab, la tabla de [archivos](file-table.md)y la transformación de idioma permite a la herramienta de combinación omitir los archivos adicionales almacenados en el archivo. cab que no aparecen en la tabla de [archivos](file-table.md). Pueden existir otros archivos en el archivo. cab, pero no deben aparecer en la [tabla de archivos](file-table.md). Por ejemplo, un módulo que instala Code.dll, English. dat, alemán. dat y francés. dat puede usar el siguiente orden de secuencia de archivos global.



| Archivo        | Secuencia |
|-------------|----------|
| Code.Dll    | 1        |
| Inglés. dat | 2        |
| Alemán. dat  | 3        |
| Francés. dat  | 4        |



 

A continuación, se pueden crear transformaciones de lenguaje para modificar la [tabla de archivos](file-table.md) del módulo para inglés, alemán o francés.

[Tabla de archivos](file-table.md) (parcial para inglés)



| Archivo        | Secuencia |
|-------------|----------|
| Code.Dll    | 1        |
| Inglés. dat | 2        |



 

[Tabla de archivos](file-table.md) (parcial para alemán)



| Archivo       | Secuencia |
|------------|----------|
| Code.Dll   | 1        |
| Alemán. dat | 3        |



 

[Tabla de archivos](file-table.md) (parcial para francés)



| Archivo       | Secuencia |
|------------|----------|
| Code.Dll   | 1        |
| Francés. dat | 4        |



 

Para obtener más información, vea [crear una transformación de lenguaje para un módulo de combinación de varios idiomas](authoring-a-language-transform-for-a-multiple-language-merge-module.md) y tablas de archivos de módulo de combinación de [creación](authoring-merge-module-file-tables.md).

 

 



