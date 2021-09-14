---
description: La tabla ActionText contiene texto que se mostrará en un cuadro de diálogo de progreso y se escribirá en el registro para las acciones que llevan mucho tiempo en ejecutarse. El texto mostrado consta de la descripción de la acción y, opcionalmente, de los datos con formato de la acción.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: ActionText (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159228"
---
# <a name="actiontext-table"></a>ActionText (tabla)

La tabla ActionText contiene texto que se mostrará en un cuadro de diálogo de progreso y se escribirá en el registro para las acciones que llevan mucho tiempo en ejecutarse. El texto mostrado consta de la descripción de la acción y, opcionalmente, de los datos con formato de la acción.

La tabla ActionText tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Acción      | [Identificador](identifier.md) | Y   | N        |
| Descripción | [Texto](text.md)             | N   | Y        |
| Plantilla    | [Plantilla](template.md)     | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Nombre de la acción.

Clave de tabla principal.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción localizada que se muestra en el cuadro de diálogo de progreso o que se escribe en el registro cuando se ejecuta la acción.

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Plantilla
</dt> <dd>

Plantilla de formato localizado que se usa para dar formato a los registros de datos de acción que se mostrarán durante la ejecución de la acción. Si no se proporciona una plantilla, no se muestran los datos de acción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Normalmente, las entradas de la tabla ActionText hacen referencia a las acciones de las tablas de secuencia. Hay otras acciones que realiza el instalador que no aparecen en la tabla de secuencias, pero que todavía deben especificarse en la tabla. En la tabla siguiente se identifican las entradas de tabla necesarias en las que el nombre de la acción y la plantilla deben crearse exactamente como se muestra, pero la descripción se puede personalizar.



| Acción          | Descripción                             | Plantilla |
|-----------------|-----------------------------------------|----------|
| Reversión        | Deshace acciones.                         | \[1\]    |
| RollbackCleanup | Quita los archivos antiguos.                      | \[1\]    |
| GenerateScript  | Genera operaciones del sistema para la acción. | \[1\]    |



 

> [!Note]  
> El texto de la acción solo se muestra para las acciones que se ejecutan dentro del script de instalación. Por lo tanto, el texto de la acción solo se muestra para las acciones que se secuencian entre las acciones [InstallInitialize](installinitialize-action.md) [e InstallFinalize.](installfinalize-action.md)

 

Puede importar una tabla ActionText localizada en la base de datos mediante Msidb.exe [**o MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). El SDK incluye una tabla ActionText localizada para cada uno de los idiomas enumerados en la sección Localización de las tablas [Error y ActionText.](localizing-the-error-and-actiontext-tables.md) Si no se rellena la tabla ActionText, el instalador carga cadenas localizadas para el idioma especificado por la [**propiedad ProductLanguage.**](productlanguage.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



