---
description: ICE58 comprueba que la tabla de medios no tiene más de 80 filas.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002561"
---
# <a name="ice58"></a>ICE58

ICE58 comprueba que la [tabla de medios](media-table.md) no tiene más de 80 filas.

## <a name="result"></a>Resultado

Las advertencias que emite ICE58 provocan un error en la instalación a menos que el paquete se instale con Windows Installer 2,0 o posterior. A partir de Windows Installer 2,0, se quita la restricción a más de 80 entradas de la tabla de medios. No se emite ninguna advertencia si la propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) del paquete es mayor o igual que 150. Los paquetes del esquema 200 o superior solo se pueden instalar mediante Windows Installer 2,0 o posterior.

## <a name="example"></a>Ejemplo

ICE58 notifica los siguientes errores y advertencias para el ejemplo que se muestra.

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

Para corregir este error, elimine las entradas de la tabla de medios no utilizadas, consolide las entradas de la tabla de medios que hacen referencia a los mismos medios y reempaquete la aplicación para reducir el contenido multimedia necesario.

[Tabla de medios](media-table.md) (parcial)



| Detectaron | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



