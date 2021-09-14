---
description: ICE06 comprueba cada tabla para validar que todas las columnas enumeradas en la \_ tabla Validación están presentes en la tabla. Si no existe una tabla, se omiten las entradas de validación \_ de esa tabla.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074676"
---
# <a name="ice06"></a>ICE06

ICE06 comprueba cada tabla para validar que todas las columnas enumeradas en la [ \_ tabla Validación](-validation-table.md) están presentes en la tabla. Si no existe una tabla, se omiten las entradas de validación \_ de esa tabla.

El propósito de ICE06 es detectar instancias en las que un autor intenta usar una nueva tabla de validación que refleja un cambio de esquema con una base de datos antigua que no se ha \_ actualizado. ICE06 también detecta el caso inverso de una tabla de validación antigua que \_ se usa con una base de datos modificada.

Tenga en cuenta que la validación interna realizada por [ICE03](ice03.md) detecta la instancia de una columna de tabla no definida en la tabla Validación que se muestra en el \_ catálogo de columnas. Por lo tanto, el uso de ICE03 y ICE06 garantiza que se prueban todas las columnas de la base de datos.

## <a name="result"></a>Resultado

ICE06 publica un error cuando hay una columna de tabla definida en la tabla Validación que \_ no aparece en la tabla \_ Columnas.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente ICE06 publica el mensaje

Columna: Versión de la tabla: ModuleSignature no está definido en la base de datos.

[ \_ Tabla de validación](-validation-table.md) (parcial)



| Tabla           | Columna   |
|-----------------|----------|
| ModuleSignature | ModuleID |
| ModuleSignature | Versión  |



 

[ \_ Tabla de columnas](-columns-table.md) (parcial)



| Tabla           | número | NOMBRE     |
|-----------------|--------|----------|
| ModuleSignature | 1      | ModuleID |



 

La columna Version de la tabla ModuleSignature no está en la base de datos ni aparece en la \_ tabla Columns.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



