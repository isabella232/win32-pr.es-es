---
description: ICE06 comprueba cada tabla para comprobar que todas las columnas enumeradas en la \_ tabla de validación están presentes en la tabla. Si no existe una tabla, \_ se omiten las entradas de validación de esa tabla.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002258"
---
# <a name="ice06"></a>ICE06

ICE06 comprueba cada tabla para comprobar que todas las columnas enumeradas en la [ \_ tabla de validación](-validation-table.md) están presentes en la tabla. Si no existe una tabla, \_ se omiten las entradas de validación de esa tabla.

El propósito de ICE06 es detectar las instancias en las que un autor intenta usar una nueva \_ tabla de validación que refleja un cambio de esquema con una base de datos antigua que no se ha actualizado. ICE06 también detecta el caso inverso de una \_ tabla de validación anterior que se utiliza con una base de datos modificada.

Tenga en cuenta que la validación interna realizada por [ICE03](ice03.md) detecta la instancia de una columna de tabla no definida en la \_ tabla de validación que aparece en el catálogo de columnas. Por lo tanto, el uso de ICE03 y ICE06 garantiza que se prueban todas las columnas de la base de datos.

## <a name="result"></a>Resultado

ICE06 expone un error cuando hay una columna de tabla definida en la \_ tabla de validación que no aparece en la \_ tabla de columnas.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE06 envía el mensaje.

Columna: versión de la tabla: ModuleSignature no está definido en la base de datos.

[ \_ Tabla de validación](-validation-table.md) (parcial)



| Tabla           | Columna   |
|-----------------|----------|
| ModuleSignature | ModuleID |
| ModuleSignature | Versión  |



 

[ \_ Tabla de columnas](-columns-table.md) (parcial)



| Tabla           | número | NOMBRE     |
|-----------------|--------|----------|
| ModuleSignature | 1      | ModuleID |



 

La columna version de la tabla ModuleSignature no está en la base de datos ni se muestra en la \_ tabla columnas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



