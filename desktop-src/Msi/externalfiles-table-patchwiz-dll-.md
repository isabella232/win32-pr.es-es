---
description: La tabla ExternalFiles contiene información sobre archivos específicos que no forman parte de una imagen de destino normal.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Tabla ExternalFiles (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544286"
---
# <a name="externalfiles-table-patchwizdll"></a>Tabla ExternalFiles (Patchwiz.dll)

La tabla ExternalFiles contiene información sobre archivos específicos que no forman parte de una imagen de destino normal. Estos archivos pueden existir en productos que han sido actualizados por otro producto, actualización o revisión. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La tabla ExternalFiles tiene las columnas siguientes.



| Columna        | Tipo    | Clave | Nullable |
|---------------|---------|-----|----------|
| Familia        | text    | Y   | N        |
| FTK           | text    | Y   | N        |
| FilePath      | text    | Y   | N        |
| SymbolPaths   | text    |     | Y        |
| IgnoreOffsets | text    |     | Y        |
| IgnoreLengths | text    |     | Y        |
| RetainOffsets | text    |     | N        |
| Pedido         | integer |     | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia
</dt> <dd>

Clave externa para la columna Family de la [tabla ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave externa en la [tabla de archivos](file-table.md) del archivo. msi de la imagen actualizada.

</dd> <dt>

<span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath
</dt> <dd>

Ruta de acceso completa del archivo externo, incluido el nombre de archivo. El campo FilePath se usa para buscar el archivo especificado en la columna FTK.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Ruta de acceso completa busca archivos de símbolos del archivo especificado en la columna FTK.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a omitir en el archivo externo. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreLengths. Esta columna es opcional.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

El valor de este campo es una lista delimitada por comas de longitudes de intervalo en bytes para los intervalos que se van a omitir en el archivo externo. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreOffsets. Esta columna es opcional.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a conservar en el archivo externo. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainOffsets del registro correspondiente en la [tabla FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Si se especifican dos o más versiones para el mismo archivo externo, la tabla puede contener varios registros con valores coincidentes en los campos FTK y Family. En este caso, el campo orden puede especificar el orden de los archivos externos que se utilizarán al crear la revisión. El orden es de la versión más antigua a la más reciente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla acepta las variables de entorno como rutas de acceso a partir de la versión 4,0 de Patchwiz.dll.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



