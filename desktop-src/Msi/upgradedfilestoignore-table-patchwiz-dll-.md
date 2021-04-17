---
description: La tabla UpgradedFilesToIgnore evita la actualización de archivos específicos que se han modificado en la imagen actualizada con respecto a las imágenes de destino.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabla UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653023"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>Tabla UpgradedFilesToIgnore (Patchwiz.dll)

La tabla UpgradedFilesToIgnore evita la actualización de archivos específicos que se han modificado en la imagen actualizada con respecto a las imágenes de destino. Puede ser útil para hacer esto en ciertos casos. Por ejemplo, un paquete de revisión diseñado únicamente para su uso con instalaciones no administrativas no necesita incluir archivos de revisión que solo formen parte de las imágenes administrativas. La exclusión de estos archivos usados únicamente en imágenes administrativas puede reducir el tamaño del paquete de revisión; sin embargo, se debe informar a los administradores sobre cómo actualizar estos archivos por separado. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La tabla UpgradedFilesToIgnore tiene las columnas siguientes.



| Columna   | Tipo | Clave | Nullable |
|----------|------|-----|----------|
| Upgraded | text | Y   | N        |
| FTK      | text | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado
</dt> <dd>

Clave externa para la columna actualizada de la [tabla UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md). La herramienta de creación de revisiones excluye la actualización del archivo especificado en la columna FTK de la tabla UpgradedFilesToIgnore al actualizar un destino a la imagen especificada en el campo actualizado. Escriba un valor de " \* " en el campo actualizado para excluir la actualización del archivo para todas las imágenes actualizadas.

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave externa en la [tabla de archivos](file-table.md) de la imagen actualizada. Un valor de la forma " <prefix> \* " coincide con todas las claves de la tabla de archivos que comienzan con ese prefijo. Ningún texto puede seguir el asterisco.

</dd> </dl>

 

 



