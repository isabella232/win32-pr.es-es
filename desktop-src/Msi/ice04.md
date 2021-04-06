---
description: ICE04 valida que el número de secuencia de todos los archivos de la tabla de archivos sea menor o igual que el número de secuencia más grande de la columna LastSequence de la tabla de medios.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002259"
---
# <a name="ice04"></a>ICE04

ICE04 valida que el número de secuencia de todos los archivos de la [tabla de archivos](file-table.md) sea menor o igual que el número de secuencia más grande de la columna LastSequence de la tabla de [medios](media-table.md).

Cada registro de la tabla de medios representa un disco en el medio de origen que contiene todos los archivos con un número de secuencia menor o igual que el valor de la columna LastSequence y mayor que el valor de LastSequence en el registro del disco anterior.

## <a name="result"></a>Resultado

ICE04 envía un mensaje de error si hay un archivo con un número de secuencia mayor que el número de LastSequence mayor de los medios de origen.

## <a name="example"></a>Ejemplo

ICE04 notificaría el siguiente error para el ejemplo mostrado:

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Tabla de archivos](file-table.md) (parcial)



| Archivo   | Secuencia |
|--------|----------|
| MyFile | 210      |



 

[Tabla de medios](media-table.md) (parcial)



| Detectaron | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



