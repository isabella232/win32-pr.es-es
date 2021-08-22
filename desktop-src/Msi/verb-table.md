---
description: La tabla Verbo contiene información del verbo de comando asociada a las extensiones de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del Registro.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Tabla de verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fc546cd3db5fecb3861120fa15b1ffa3f21327b889599b77a1b067193c886c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499115"
---
# <a name="verb-table"></a>Tabla de verbos

La tabla Verbo contiene información del verbo de comando asociada a las extensiones de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del Registro.

La tabla Verbo tiene las columnas siguientes.



| Columna      | Tipo                       | Clave | Nullable |
|-------------|----------------------------|-----|----------|
| Extensión\_ | [Texto](text.md)           | Y   | N        |
| Verbo        | [Texto](text.md)           | Y   | N        |
| Secuencia    | [Entero](integer.md)     | N   | Y        |
| Get-Help     | [Formato](formatted.md) | N   | Y        |
| Argumento    | [Formato](formatted.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extensión\_
</dt> <dd>

Extensión asociada a la fila de tabla. Esta columna es una clave externa a la primera columna de la [tabla De extensión](extension-table.md).

</dd> <dt>

<span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo
</dt> <dd>

Verbo del comando.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

Secuencia de los comandos. Solo se usan verbos para los que la columna Sequence es distinto de Null para preparar una lista ordenada para el valor predeterminado de la clave de shell. El verbo con el valor más bajo de esta columna se convierte en el verbo predeterminado.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Comando
</dt> <dd>

Texto localizable que se muestra en el menú contextual.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

Valor de los argumentos del comando.

Tenga en cuenta que la resolución de propiedades en el campo Argument es limitada. Una propiedad con el formato Propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando se instala el componente propietario \[  \] del verbo. Por ejemplo, para que el argumento "MyDoc.doc" se resuelva en el valor correcto, el mismo proceso debe instalar el archivo MyDoc.doc y el componente que posee el \[ \# \] verbo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se hace referencia a esta tabla cuando se ejecuta [la acción RegisterExtensionInfo](registerextensioninfo-action.md) o la acción [UnregisterExtensionInfo.](unregisterextensioninfo-action.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



