---
description: La \_ tabla UpgradedFile OptionalData contiene información sobre los archivos específicos de una imagen actualizada. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Tabla UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279008"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>UpgradedFiles \_ OptionalData (Patchwiz.dll)

La \_ tabla UpgradedFile OptionalData contiene información sobre los archivos específicos de una imagen actualizada. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La \_ tabla UpgradedFile OptionalData tiene las columnas siguientes.



| Columna                  | Tipo    | Clave | Nullable |
|-------------------------|---------|-----|----------|
| Upgraded                | text    | Y   | N        |
| FTK                     | text    | Y   | N        |
| SymbolPaths             | text    |     | Y        |
| AllowIgnoreOnPatchError | integer |     | Y        |
| IncludeWholeFile        | integer |     | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado
</dt> <dd>

Clave externa para la columna actualizada de la [tabla UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave de la tabla de archivos. Clave externa en la [tabla de archivos](file-table.md) del archivo. msi de la imagen actualizada. Si dos o más imágenes actualizadas dentro de una familia tienen el mismo valor de FTK, el valor debe hacer referencia al mismo archivo. Los archivos compartidos por varias imágenes de actualización deben tener el mismo FTK para minimizar el tamaño del archivo. cab.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

El valor de este campo se agrega a la lista de carpetas delimitada por signos de punto y coma en la columna SymbolPaths de la [tabla UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) cuando se genera la revisión, y se puede usar para agregar archivos de símbolos para un archivo específico.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

Establézcalo en 1 para indicar que la revisión no es fundamental. Establézcalo en 0 para indicar que la revisión es fundamental. Si Windows Installer encuentra un problema al aplicar esta revisión al archivo especificado en la columna FTK, el valor de este campo determinará si el cuadro de mensaje de error incluye un botón **omitir** para permitir que el usuario continúe el proceso de aplicación de revisiones.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

Establezca en un valor distinto de cero si se debe instalar el archivo completo especificado en la columna FTK en lugar de crear una revisión binaria.

</dd> </dl>

 

 



