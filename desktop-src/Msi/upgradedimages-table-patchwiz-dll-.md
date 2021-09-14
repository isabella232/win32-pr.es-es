---
description: La tabla UpgradedImages contiene información sobre las imágenes actualizadas del producto.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Tabla UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254097"
---
# <a name="upgradedimages-table-patchwizdll"></a>Tabla UpgradedImages (Patchwiz.dll)

La tabla UpgradedImages contiene información sobre las imágenes actualizadas del producto. La imagen actualizada debe ser una imagen de configuración completamente sin comprimir de la versión más reciente del producto, por ejemplo, una imagen administrativa o una imagen de instalación sin comprimir desde un CD-ROM. Un Windows de revisión del instalador actualiza una imagen de destino en una imagen actualizada. La tabla UpgradedImages es necesaria en la base de datos de creación de revisiones (archivo .csv) y la [usa UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

Se requiere una tabla UpgradedImages que contenga al menos un registro en cada base de datos de creación de revisiones (archivo .csv). [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)usa esta tabla.

La tabla UpgradedImages tiene las columnas siguientes.



| Columna       | Tipo | Clave | Nullable |
|--------------|------|-----|----------|
| Upgraded     | text | Y   | No        |
| MsiPath      | text |     | No        |
| PatchMsiPath | text |     | Y        |
| SymbolPaths  | text |     | Y        |
| Familia       | text |     | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado
</dt> <dd>

El campo Actualizado es un identificador arbitrario para conectar las imágenes de destino con una imagen actualizada del producto.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Este campo especifica la ruta de acceso completa, incluido el nombre de archivo, a la ubicación del archivo .msi para la imagen actualizada. Esta es la ubicación de los archivos de origen de la imagen actualizada.

</dd> <dt>

<span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath
</dt> <dd>

El patchMsiPath opcional apunta a una copia modificada de la base de datos de instalación actualizada que contiene una creación adicional específica del proceso de instalación de revisiones. Por ejemplo, cuadros de diálogo adicionales o acciones personalizadas que están condicióndas en la [**propiedad PATCH.**](patch.md)

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Lista delimitada por punto y coma de carpetas en las que se van a buscar archivos de símbolos que se pueden usar para optimizar la generación de la revisión binaria. Tenga en cuenta que no se buscan los subdirectorios de las carpetas especificadas en este campo. Una revisión binaria optimizada puede ser más pequeña. Visual C++ debe instalarse en el equipo que genera la revisión y usarse para crear los archivos de símbolos. Este campo es opcional y el instalador crea una revisión binaria incluso si no se especifica ningún archivo de símbolos o si los archivos de símbolos no están disponibles para Patchwiz.dll.

</dd> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia
</dt> <dd>

Clave externa en la [tabla ImageFamilies](imagefamilies-table-patchwiz-dll-.md). Cada imagen actualizada debe pertenecer a una sola familia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Aunque cada imagen actualizada se puede agrupar en una familia de imágenes independiente, la agrupación de imágenes actualizadas que comparten archivos puede hacer que el archivo .msp sea más pequeño.

Esta tabla acepta variables de entorno como rutas de acceso a partir de la versión 4.0 de Patchwiz.dll.

 

 



