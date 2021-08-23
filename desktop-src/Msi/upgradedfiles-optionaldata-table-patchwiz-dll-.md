---
description: La tabla UpgradedFile \_ OptionalData contiene información sobre archivos específicos de una imagen actualizada. Esta tabla es opcional en la base de datos de creación de revisiones (archivo .csv) y la usa la función UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: UpgradedFiles_OptionalData tabla (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eb766f8db9d295546670c80627284991da1ff8dccb5a0c2900be74bd785dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012843"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>Tabla UpgradedFiles \_ OptionalData (Patchwiz.dll)

La tabla UpgradedFile \_ OptionalData contiene información sobre archivos específicos de una imagen actualizada. Esta tabla es opcional en la base de datos de creación de revisiones (archivo .csv) y la usa la [función UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabla UpgradedFile \_ OptionalData tiene las columnas siguientes.



| Columna                  | Tipo    | Clave | Nullable |
|-------------------------|---------|-----|----------|
| Upgraded                | texto    | Y   | N        |
| FTK                     | texto    | Y   | N        |
| SymbolPaths             | texto    |     | Y        |
| AllowIgnoreOnPatchError | integer |     | Y        |
| IncludeWholeFile        | integer |     | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado
</dt> <dd>

Clave externa a la columna Actualizado de [la tabla UpgradedImages (Patchwiz.dll).](upgradedimages-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave de tabla de archivo. Clave externa en [la tabla File](file-table.md) del .msi archivo de la imagen actualizada. Si dos o más imágenes actualizadas dentro de una familia tienen el mismo valor de FTK, el valor debe hacer referencia al mismo archivo. Los archivos compartidos por varias imágenes de actualización deben tener la misma FTK para minimizar el tamaño de archivo del archivador.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

El valor de este campo se agrega a la lista de carpetas delimitada por punto y coma de la columna SymbolPaths de la tabla [UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) cuando se genera la revisión y se puede usar para agregar archivos de símbolos para un archivo específico.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

Establezca en 1 para indicar que la revisión no es vital. Establezca en 0 para indicar que la revisión es vital. Si Windows Installer encuentra un problema al aplicar esta revisión al archivo especificado en la columna FTK, el valor  de este campo determina si el cuadro de mensaje de error incluye un botón Omitir para permitir al usuario continuar con el proceso de aplicación de revisiones.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

Establezca en un valor distinto de cero si se debe instalar todo el archivo especificado en la columna FTK en lugar de crear una revisión binaria.

</dd> </dl>

 

 



