---
description: ICE98 comprueba el campo de descripción de la tabla ODBCDataSource para un origen de datos ODBC. Usa la función SQLValidDSN para comprobar que solo se usan caracteres válidos y que la descripción no supera la longitud máxima permitida.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f8a627b057e6c235fdb57a4f2d5d2b2cf6274e528ef4945c6a6323e1888427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894695"
---
# <a name="ice98"></a>ICE98

ICE98 comprueba el campo de descripción de la tabla [ODBCDataSource para](odbcdatasource-table.md) un origen de datos ODBC. Usa la **función SQLValidDSN** para comprobar que solo se usan caracteres válidos y que la descripción no supera la longitud máxima permitida.

## <a name="result"></a>Resultado

ICE98 publica las siguientes advertencias.



| Advertencia ice98                    | Descripción                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El nombre del origen de datos no es válido. | El valor de la columna Descripción de la tabla [ODBCDataSource](odbcdatasource-table.md) contiene caracteres no válidos o es demasiado largo, lo que significa que supera SQL \_ MAX DSN LENGTH de \_ \_ 32. |



 

## <a name="example"></a>Ejemplo

ICE98 notifica las siguientes advertencias para el ejemplo:

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

[Tabla ODBCDataSource](odbcdatasource-table.md) (parcial)



| DataSource | Descripción                      |
|------------|----------------------------------|
| BadChar    | !                                |
| TooLong    | <String of length > 32> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> <dt>

[Tabla ODBCDataSource](odbcdatasource-table.md)
</dt> </dl>

 

 



