---
description: La tabla UpgradedImages contiene información sobre las imágenes actualizadas del producto.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Tabla UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361390"
---
# <a name="upgradedimages-table-patchwizdll"></a>Tabla UpgradedImages (Patchwiz.dll)

La tabla UpgradedImages contiene información sobre las imágenes actualizadas del producto. La imagen actualizada debe ser una imagen de instalación totalmente descomprimida de la versión más reciente del producto, por ejemplo, una imagen administrativa o una imagen de instalación sin comprimir de un CD-ROM. Un paquete de revisión de Windows Installer actualiza una imagen de destino en una imagen actualizada. La tabla UpgradedImages es necesaria en la base de datos de creación de revisiones (archivo. PCP) y se usa en [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).

Se requiere una tabla UpgradedImages que contenga al menos un registro en cada base de datos de creación de revisiones (archivo. PCP). Esta tabla la usa [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).

La tabla UpgradedImages tiene las columnas siguientes.



| Columna       | Tipo | Clave | Nullable |
|--------------|------|-----|----------|
| Upgraded     | text | Y   | N        |
| Rutamsi      | text |     | N        |
| PatchMsiPath | text |     | Y        |
| SymbolPaths  | text |     | Y        |
| Familia       | text |     | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado
</dt> <dd>

El campo actualizado es un identificador arbitrario para conectar las imágenes de destino con una imagen actualizada del producto.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>Rutamsi
</dt> <dd>

Este campo especifica la ruta de acceso completa, incluido el nombre de archivo, en la ubicación del archivo. msi de la imagen actualizada. Esta es la ubicación de los archivos de origen de la imagen actualizada.

</dd> <dt>

<span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath
</dt> <dd>

El patchMsiPath opcional apunta a una copia modificada de la base de datos de instalación actualizada que contiene la creación adicional específica del proceso de instalación de la revisión. Por ejemplo, cuadros de diálogo adicionales o acciones personalizadas condicionadas en la propiedad [**patch**](patch.md) .

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Una lista delimitada por punto y coma de carpetas en las que se van a buscar archivos de símbolos que se pueden usar para optimizar la generación de la revisión binaria. Tenga en cuenta que no se busca en los subdirectorios de las carpetas especificadas en este campo. Una revisión binaria optimizada puede ser menor. Visual C++ debe estar instalado en el equipo que genera la revisión y que se usa para crear los archivos de símbolos. Este campo es opcional y el instalador crea una revisión binaria incluso si no se especifica ningún archivo de símbolos o si los archivos de símbolos dejan de estar disponibles para Patchwiz.dll.

</dd> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia
</dt> <dd>

Clave externa en la [tabla ImageFamilies](imagefamilies-table-patchwiz-dll-.md). Cada imagen actualizada debe pertenecer a una sola familia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Aunque cada imagen actualizada se puede agrupar en una familia de imágenes independiente, la agrupación de imágenes actualizadas que compartan archivos juntos puede hacer que el archivo. MSP sea más pequeño.

Esta tabla acepta las variables de entorno como rutas de acceso a partir de la versión 4,0 de Patchwiz.dll.

 

 



