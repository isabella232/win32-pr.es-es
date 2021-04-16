---
description: La tabla Verb contiene información de verbo de comando asociada a las extensiones de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del registro.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Tabla de verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678585"
---
# <a name="verb-table"></a>Tabla de verbos

La tabla Verb contiene información de verbo de comando asociada a las extensiones de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del registro.

La tabla de verbos tiene las columnas siguientes.



| Columna      | Tipo                       | Clave | Nullable |
|-------------|----------------------------|-----|----------|
| Extensión\_ | [Texto](text.md)           | Y   | N        |
| Verbo        | [Texto](text.md)           | Y   | N        |
| Secuencia    | [Entero](integer.md)     | N   | Y        |
| Get-Help     | [Formatea](formatted.md) | N   | Y        |
| Argumento    | [Formatea](formatted.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_
</dt> <dd>

La extensión asociada a la fila de la tabla. Esta columna es una clave externa de la primera columna de la [tabla de extensión](extension-table.md).

</dd> <dt>

<span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Solicitud
</dt> <dd>

El verbo para el comando.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ
</dt> <dd>

Secuencia de comandos. Solo los verbos para los que la columna de secuencia no es NULL se utilizan para preparar una lista ordenada para el valor predeterminado de la clave de Shell. El verbo con el valor más bajo de esta columna se convierte en el verbo predeterminado.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command
</dt> <dd>

Texto traducible que se muestra en el menú contextual.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Valor de los argumentos de comando.

Tenga en cuenta que la resolución de propiedades en el campo argumento es limitada. Una propiedad con formato \[  \] de propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando el componente propietario del verbo está instalado. Por ejemplo, para que el argumento " \[ \#MyDoc.doc\] " resuelva el valor correcto, el mismo proceso debe instalar el archivo MyDoc.doc y el componente que posee el verbo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterExtensionInfo](registerextensioninfo-action.md) o la [acción UnregisterExtensionInfo](unregisterextensioninfo-action.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



