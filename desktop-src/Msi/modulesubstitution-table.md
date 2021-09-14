---
description: La tabla ModuleSubstitution especifica los campos configurables de una base de datos de módulos y proporciona una plantilla para la configuración de cada campo.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: Tabla ModuleSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e27789f723af87e228bada91b79a16d7dc4d2d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261127"
---
# <a name="modulesubstitution-table"></a>Tabla ModuleSubstitution

La tabla ModuleSubstitution especifica los campos configurables de una base de datos de módulos y proporciona una plantilla para la configuración de cada campo. El usuario o la herramienta de combinación pueden consultar esta tabla para determinar qué operaciones de configuración se van a realizar. Esta tabla no se combina con la base de datos de destino.

Las tablas siguientes no pueden contener campos configurables y no deben aparecer en esta tabla:

Tabla ModuleSubstitution

[Tabla ModuleConfiguration](moduleconfiguration-table.md)

[Tabla ModuleExclusion](moduleexclusion-table.md)

[Tabla ModuleSignature](modulesignature-table.md)

La tabla ModuleSubstitution tiene las siguientes columnas.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Tabla  | [Identificador](identifier.md) | Y   | N        |
| Row    | [Texto](text.md)             | Y   | N        |
| Columna | [Identificador](identifier.md) | Y   | N        |
| Value  | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Mesa
</dt> <dd>

Esta columna especifica el nombre de la tabla que se va a modificar en la base de datos del módulo.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Fila
</dt> <dd>

Este campo especifica las claves principales de la fila de destino de la tabla denominada en la columna Tabla . Varias claves principales están separadas por punto y coma. Las filas de destino se seleccionan para su modificación antes de realizar cambios en la tabla de destino. Si un registro de la tabla ModuleSubstitution cambia el campo de clave principal de una fila de destino, otros registros de la tabla ModuleSubstitution se aplican en función de los datos de clave principal originales, no del resultado de las sustituciones de clave principal. El orden de sustitución de filas es indefinido.

Los valores de esta columna siempre están en [formato especial de CMSM.](cmsm-special-format.md) Se puede agregar un signo de punto (';') literal o signo igual ('=') si se antefila el carácter con una barra diagonal inversa. '\\'. Un valor NULL para una clave se indica mediante un valor NULL, un punto y coma inicial, dos punto y coma consecutivos o un punto y coma final, dependiendo de si el valor NULL es un valor de columna de clave única, primera, intermedia o final.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Columna
</dt> <dd>

Este campo especifica la columna de destino de la fila denominada en la columna Fila. Si varias filas de la tabla ModuleSubstitution cambian columnas diferentes de la misma fila de destino, todas las sustituciones de columnas se realizan antes de insertar la fila modificada en la base de datos. El orden de sustitución de columnas no está definido.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta columna contiene una cadena que proporciona una plantilla de formato para los datos que se sustituyen en el campo de destino especificado por Tabla, Fila y Columna. Cuando se encuentra una cadena de sustitución con el formato =ItemA, la cadena, incluidos los caracteres entre corchetes, se reemplaza por el valor del \[ \] elemento configurable "ItemA". El elemento configurable "ItemA" se especifica en la columna Nombre de la tabla [ModuleConfiguration](moduleconfiguration-table.md) y su valor lo proporciona la herramienta de combinación. Si la herramienta de combinación rechaza proporcionar un valor para cualquier elemento de una cadena de reemplazo, se sustituye el valor predeterminado especificado en la columna DefaultValue de la tabla ModuleConfiguration. Si una cadena hace referencia a un elemento que no está en la tabla ModuleConfiguration, se produce un error en la combinación.

-   Esta columna usa [el formato especial cmsm](cmsm-special-format.md). Se puede agregar un signo de punto y coma literal (';') o igual a ('=') a la tabla antefiriendo el carácter con una barra diagonal inversa. '\\'.
-   El campo Valor puede contener varias cadenas de sustitución. Por ejemplo, la configuración de los elementos "Food1" y "Food2" en la cadena: " =Food1 es buena, pero =Food2 es mejor porque \[ \] \[ =Food2 es más \] \[ \] trastocario".
-   Las cadenas de reemplazo no deben estar anidadas. La plantilla " \[ =AB \[ =CDE" \] \] no es válida.
-   Si el campo Valor se evalúa como NULL y el campo de destino no acepta valores NULL, se produce un error en la combinación y se crea un objeto de error de tipo msmErrorBadNullSubstitution y se agrega a la lista de errores. Para obtener más información, vea los tipos de error descritos en [**get \_ Type Function**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).
-   Si el campo Valor se evalúa como el GUID null: , el GUID null se reemplaza por el nombre de la característica antes de que la fila se combine {00000000-0000-0000-0000-000000000000} en el módulo. Para obtener más información, vea [Hacer referencia a características en módulos de mezcla.](referencing-features-in-merge-modules.md)
-   La plantilla del campo Valor se evalúa antes de insertarse en el campo de destino. La sustitución en una fila se realiza antes de reemplazar las características.
-   Si la columna Valor se evalúa como una cadena de solo caracteres enteros (con un opcional + o -), la cadena se convierte en un entero antes de sustituirse en un campo de destino del tipo de formato entero [.](integer-format-types.md) Si la plantilla se evalúa como una cadena que no consta solo de caracteres enteros (y un opcional + o -), el resultado no se puede sustituir en un campo de destino entero. Al intentar insertar un campo que no es entero en un campo entero, se produce un error en la combinación y se agrega un objeto de error msmErrorBadSubstitutionType a la lista de errores.
-   Si la columna de destino especificada en [](text-format-types.md)los campos Tabla y Columna es un tipo de formato de texto y la evaluación del campo Valor da como resultado un tipo de formato entero [,](integer-format-types.md)se inserta una representación decimal del número en el campo de texto de destino.
-   Si el campo [](integer-format-types.md)de destino es un tipo de formato entero y el campo Valor consta de una lista no delimitada de elementos en Formato de  campo de bits [,](bitfield-format-types.md)el valor del campo de destino se combina mediante el operador **AND** bit a bit con el inverso de or bit a bit de todos los valores de máscara de los elementos y, a continuación, se combina mediante el operador **OR** bit a bit con cada uno de los elementos enteros o de campo de bits cuando se enmascaran por sus valores de máscara correspondientes. Básicamente, esto establece explícitamente los bits de las propiedades en los valores proporcionados, pero deja solos los demás bits de la celda.
-   Si el campo Valor [](key-format-types.md)se evalúa como un tipo de formato de clave y es una clave en una tabla que usa varias claves principales, el nombre del elemento puede ir seguido de un punto y coma y un valor entero que indica el índice basado en 1 en el conjunto de valores que juntos hacen una clave principal. Si no se especifica ningún entero, se usa el valor 1. Por ejemplo, la [tabla Control tiene](control-table.md) dos columnas de clave principal, Dialog y \_ Control. El valor de un elemento "Item1" que es una clave de la tabla Control tendrá el formato "DialogName; ControlName", donde DialogName es el valor de la tabla Dialog y \_ ControlName es el valor de la columna Control. Para sustituir solo ControlName, se debe usar la cadena de \[ sustitución =Item1;2. \]

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los módulos de mezcla configurables usan la tabla ModuleSubstition [.](configurable-merge-modules.md) Mergemod.dll versión 2.0 o posterior es necesario para crear un módulo de combinación configurable.

Para garantizar la compatibilidad con versiones de Mergemod.dll anteriores a la versión 2.0, las tablas [ModuleConfiguration](moduleconfiguration-table.md) y ModuleSubstitution deben incluirse en la tabla [ModuleIgnoreTable](moduleignoretable-table.md) de cada módulo.

 

 
