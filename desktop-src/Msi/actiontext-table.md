---
description: La tabla ActionText contiene el texto que se va a mostrar en un cuadro de diálogo de progreso y se escribe en el registro para las acciones que tardan mucho tiempo en ejecutarse. El texto mostrado consta de la descripción de la acción y, opcionalmente, los datos con formato de la acción.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabla de ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667059"
---
# <a name="actiontext-table"></a>Tabla de ActionText

La tabla ActionText contiene el texto que se va a mostrar en un cuadro de diálogo de progreso y se escribe en el registro para las acciones que tardan mucho tiempo en ejecutarse. El texto mostrado consta de la descripción de la acción y, opcionalmente, los datos con formato de la acción.

La tabla ActionText tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Acción      | [Identificador](identifier.md) | Y   | N        |
| Descripción | [Texto](text.md)             | N   | Y        |
| Plantilla    | [Plantilla](template.md)     | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar
</dt> <dd>

Nombre de la acción.

Clave de la tabla principal.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Descripción localizada que se muestra en el cuadro de diálogo de progreso o que se escribe en el registro cuando se ejecuta la acción.

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Plantillas
</dt> <dd>

Una plantilla de formato localizada que se utiliza para dar formato a los registros de datos de acción que se van a mostrar durante la ejecución de la acción. Si no se proporciona una plantilla, los datos de la acción no se muestran.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Normalmente, las entradas de la tabla ActionText hacen referencia a las acciones de las tablas de secuencia. Hay otras acciones que realiza el instalador y que no aparecen en la tabla de secuencia, pero que deben especificarse en la tabla. En la tabla siguiente se identifican las entradas de tabla necesarias en las que el nombre de acción y la plantilla deben crearse exactamente como se muestra, pero la descripción se puede personalizar.



| Acción          | Descripción                             | Plantilla |
|-----------------|-----------------------------------------|----------|
| Reversión        | Deshace las acciones.                         | \[1\]    |
| RollbackCleanup | Quita los archivos antiguos.                      | \[1\]    |
| GenerateScript  | Genera operaciones del sistema para la acción. | \[1\]    |



 

> [!Note]  
> El texto de la acción solo se muestra para las acciones que se ejecutan dentro del script de instalación. Por lo tanto, el texto de la acción solo se muestra para las acciones que se secuencian entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md) .

 

Puede importar una tabla de ActionText localizada en la base de datos mediante Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). El SDK incluye una tabla de ActionText localizada para cada uno de los idiomas que aparecen en la sección [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md) . Si no se rellena la tabla de ActionText, el instalador carga las cadenas localizadas para el idioma especificado por la propiedad [**ProductLanguage**](productlanguage.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



