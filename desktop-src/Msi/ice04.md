---
description: ICE04 valida que el número de secuencia de cada archivo de la tabla File es menor o igual que el número de secuencia más grande de la columna LastSequence de la tabla Media.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b77bf11d26d694a25f62db8da005139566b2c92310e2bb2dded4eecbca79719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635667"
---
# <a name="ice04"></a>ICE04

ICE04 valida que el número de [](file-table.md) secuencia de cada archivo de la tabla File es menor o igual que el número de secuencia más grande de la columna LastSequence de la [tabla Media](media-table.md).

Cada registro de la tabla Media representa un disco en el medio de origen que contiene todos los archivos con un número de secuencia menor o igual que el valor de la columna LastSequence y mayor que el valor LastSequence del registro del disco anterior.

## <a name="result"></a>Resultado

ICE04 publica un mensaje de error si hay un archivo con un número de secuencia mayor que el número de LastSequence más grande para el medio de origen.

## <a name="example"></a>Ejemplo

ICE04 notificaría el siguiente error para el ejemplo mostrado:

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Tabla de archivos](file-table.md) (parcial)



| Archivo   | Secuencia |
|--------|----------|
| Mi_archivo | 210      |



 

[Tabla multimedia](media-table.md) (parcial)



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



