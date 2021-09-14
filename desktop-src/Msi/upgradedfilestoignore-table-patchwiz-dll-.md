---
description: La tabla UpgradedFilesToIgnore impide la actualización de archivos específicos que, de hecho, se han modificado en la imagen actualizada con respecto a las imágenes de destino.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabla UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3af0a4a8c3385c2d028cdb66ad276d3f480ca8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254096"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>Tabla UpgradedFilesToIgnore (Patchwiz.dll)

La tabla UpgradedFilesToIgnore impide la actualización de archivos específicos que, de hecho, se han modificado en la imagen actualizada con respecto a las imágenes de destino. Puede ser útil hacerlo en determinados casos. Por ejemplo, un paquete de revisión diseñado solo para su uso con instalaciones no administrativas no necesita incluir archivos de aplicación de revisiones que solo forman parte de imágenes administrativas. Excluir estos archivos usados solo en imágenes administrativas puede reducir el tamaño del paquete de revisión; Sin embargo, se debe informar a los administradores sobre cómo actualizar estos archivos por separado. Esta tabla es opcional en la base de datos de creación de revisiones (archivo .fp) y la usa la función [UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabla UpgradedFilesToIgnore tiene las siguientes columnas.



| Columna   | Tipo | Clave | Nullable |
|----------|------|-----|----------|
| Upgraded | text | Y   | No        |
| FTK      | text | Y   | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado
</dt> <dd>

Clave externa a la columna Upgraded de [la tabla UpgradedImages (Patchwiz.dll).](upgradedimages-table-patchwiz-dll-.md) La herramienta de creación de revisiones excluye la actualización del archivo especificado en la columna FTK de la tabla UpgradedFilesToIgnore al actualizar un destino a la imagen especificada en el campo Actualizado. Escriba un valor de " \* " en el campo Actualizado para excluir la actualización del archivo para todas las imágenes actualizadas.

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave externa en la [tabla Archivo](file-table.md) de la imagen actualizada. Un valor con el formato " prefijo " coincide con todas las claves de tabla de archivos de &lt; la tabla File que &gt; \* comienzan por ese prefijo. Ningún texto puede seguir el asterisco.

</dd> </dl>

 

 



