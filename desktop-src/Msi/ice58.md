---
description: ICE58 comprueba que la tabla Media no tiene más de 80 filas.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be8cec8fda3a3ddc1efce397dfbd17a95a2baf37ab0392eb8e5ffd08c7df4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528235"
---
# <a name="ice58"></a>ICE58

ICE58 comprueba que la [tabla Media](media-table.md) no tiene más de 80 filas.

## <a name="result"></a>Resultado

Las advertencias notificadas por ICE58 hacen que la instalación no se pueda instalar a menos que el paquete se instale con Windows Installer 2.0 o posterior. A partir Windows Installer 2.0, se quita la restricción a más de 80 entradas de tabla multimedia. No se emite ninguna advertencia si la propiedad [**Resumen**](page-count-summary.md) de recuento de páginas del paquete es mayor o igual que 150. Los paquetes del esquema 200 o posterior solo se pueden instalar Windows Installer 2.0 o posterior.

## <a name="example"></a>Ejemplo

ICE58 notifica los siguientes errores y advertencias para el ejemplo mostrado.

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

Para corregir este error, elimine las entradas de tabla multimedia no utilizadas, consolide las entradas de tabla multimedia que hacen referencia al mismo medio y vuelva a empaquetar la aplicación para reducir los medios necesarios.

[Tabla multimedia](media-table.md) (parcial)



| DiskId | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



