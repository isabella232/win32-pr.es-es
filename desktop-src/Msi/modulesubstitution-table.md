---
description: La tabla ModuleSubstitution especifica los campos configurables de una base de datos de módulos y proporciona una plantilla para la configuración de cada campo.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: Tabla ModuleSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e27789f723af87e228bada91b79a16d7dc4d2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279343"
---
# <a name="modulesubstitution-table"></a>Tabla ModuleSubstitution

La tabla ModuleSubstitution especifica los campos configurables de una base de datos de módulos y proporciona una plantilla para la configuración de cada campo. El usuario o la herramienta de combinación puede consultar esta tabla para determinar qué operaciones de configuración tienen lugar. Esta tabla no se combina en la base de datos de destino.

Las tablas siguientes no pueden contener campos configurables y no deben aparecer en esta tabla:

Tabla ModuleSubstitution

[Tabla ModuleConfiguration](moduleconfiguration-table.md)

[Tabla ModuleExclusion](moduleexclusion-table.md)

[ModuleSignature (tabla)](modulesignature-table.md)

La tabla ModuleSubstitution tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Tabla  | [Identificador](identifier.md) | Y   | N        |
| Row    | [Texto](text.md)             | Y   | N        |
| Columna | [Identificador](identifier.md) | Y   | N        |
| Value  | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro
</dt> <dd>

Esta columna especifica el nombre de la tabla que se está modificando en la base de datos del módulo.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Columna
</dt> <dd>

Este campo especifica las claves principales de la fila de destino de la tabla denominada en la columna de la tabla. Varias claves principales se separan mediante signos de punto y coma. Las filas de destino se seleccionan para modificarlas antes de que se realicen cambios en la tabla de destino. Si un registro de la tabla ModuleSubstitution cambia el campo de clave principal de una fila de destino, se aplican otros registros de la tabla ModuleSubstitution en función de los datos de la clave principal original, no del resultado de las sustituciones de clave principal. El orden de sustitución de filas es indefinido.

Los valores de esta columna están siempre en [formato especial de CMsM](cmsm-special-format.md). Se puede Agregar un carácter de punto y coma ('; ') o un signo igual (' = ') literal prefijando el carácter con una barra diagonal inversa. '\\'. Un valor null para una clave se indica mediante un valor null, un punto y coma inicial, dos puntos y comas consecutivos, o un punto y coma final, en función de si el valor NULL es un valor de columna de clave único, primero, medio o final.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Artículo
</dt> <dd>

Este campo especifica la columna de destino de la fila denominada en la columna Row. Si varias filas de la tabla ModuleSubstitution cambian columnas diferentes de la misma fila de destino, se realizan todas las sustituciones de columna antes de que se inserte la fila modificada en la base de datos. El orden de sustitución de la columna es indefinido.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta columna contiene una cadena que proporciona una plantilla de formato para los datos que se sustituyen en el campo de destino especificado por tabla, fila y columna. Cuando se encuentra una cadena de sustitución \[ con el formato Itema \] , la cadena, incluidos los caracteres de corchete, se reemplaza por el valor de la opción configurable "Itema". El elemento configurable "Itema" se especifica en la columna Name de la [tabla ModuleConfiguration](moduleconfiguration-table.md) y la herramienta de combinación proporciona su valor. Si la herramienta de combinación declina proporcionar un valor para cualquier elemento de una cadena de reemplazo, se sustituirá el valor predeterminado especificado en la columna DefaultValue de la tabla ModuleConfiguration. Si una cadena hace referencia a un elemento que no está en la tabla ModuleConfiguration, se produce un error en la combinación.

-   Esta columna usa el [formato especial de CMsM](cmsm-special-format.md). Un carácter de punto y coma ('; ') o signo igual (' = ') literal se puede Agregar a la tabla prefijando el carácter con una barra diagonal inversa. '\\'.
-   El campo de valor puede contener varias cadenas de sustitución. Por ejemplo, la configuración de los elementos "Food1" y "Food2" en la cadena: " \[ = Food1 \] es buena, pero \[ = Food2 \] es mejor porque \[ = Food2 \] es más Nutritious".
-   Las cadenas de reemplazo no deben estar anidadas. La plantilla " \[ = AB \[ = CDE \] \] " no es válida.
-   Si el campo de valor se evalúa como NULL y el campo de destino no admite valores NULL, se produce un error en la combinación y se crea un objeto de error de tipo msmErrorBadNullSubstitution y se agrega a la lista de errores. Para obtener más información, consulte los tipos de error descritos en [**\_ función de tipo Get**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).
-   Si el campo de valor se evalúa como el GUID NULL: {00000000-0000-0000-0000-000000000000} , el GUID NULL se reemplaza por el nombre de la característica antes de que la fila se combine en el módulo. Para obtener más información, vea [hacer referencia a características en módulos de combinación](referencing-features-in-merge-modules.md).
-   La plantilla en el campo valor se evalúa antes de insertarse en el campo de destino. La sustitución en una fila se realiza antes de reemplazar las características.
-   Si la columna de valor se evalúa como una cadena de caracteres enteros solamente (con un opcional + o-), la cadena se convierte en un entero antes de sustituirse en un campo de destino con el [tipo de formato entero](integer-format-types.md). Si la plantilla se evalúa como una cadena que no consta solo de caracteres enteros (y un opcional + o-), el resultado no se puede sustituir en un campo de destino de tipo entero. Si se intenta insertar un valor no entero en un campo entero, se produce un error en la combinación y se agrega un objeto de error msmErrorBadSubstitutionType a la lista de errores.
-   Si la columna de destino especificada en los campos tabla y columna es un [tipo de formato de texto](text-format-types.md)y la evaluación del campo de valor da como resultado un tipo de [formato entero](integer-format-types.md), se inserta una representación decimal del número en el campo de texto de destino.
-   Si el campo de destino es [un tipo de formato entero](integer-format-types.md), y el campo de valor consta de una lista de elementos no delimitados en formato de tipo de [bits](bitfield-format-types.md), el valor del campo de destino se combina utilizando **el operador and bit a bit** con el inverso de **la operación OR bit a bit** de todos los valores de máscara de los elementos y, a continuación, se combina utilizando el operador OR bit a bit con cada uno de los elementos **enteros o de** En esencia, esto establece explícitamente los bits de las propiedades en los valores proporcionados pero deja todos los demás bits en la celda.
-   Si el campo de valor se evalúa como un [tipo de formato de clave](key-format-types.md)y es una clave en una tabla que usa varias claves principales, el nombre del elemento puede ir seguido de un punto y coma y un valor entero que indica el índice basado en 1 en el conjunto de valores que juntas hacen referencia a una clave principal. Si no se especifica ningún entero, se utiliza el valor 1. Por ejemplo, la [tabla de control](control-table.md) tiene dos columnas de clave principal, cuadro de diálogo \_ y control. El valor de un elemento "Item1" que es una clave en la tabla de control tendrá el formato "DialogName; Nombrecontrol ", donde DialogName es el valor de la tabla del cuadro de diálogo \_ y ControlName es el valor de la columna control. Para sustituir solo nombrecontrol, se debe usar la cadena de sustitución \[ = Item1; 2 \] .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los [módulos de combinación configurables](configurable-merge-modules.md)usan la tabla ModuleSubstition. Se necesita Mergemod.dll versión 2,0 o posterior para crear un módulo de combinación configurable.

Para garantizar la compatibilidad con versiones de Mergemod.dll anteriores a la versión 2,0, las tablas [ModuleConfiguration](moduleconfiguration-table.md) y ModuleSubstitution se deben incluir en la [tabla ModuleIgnoreTable](moduleignoretable-table.md) de cada módulo.

 

 
