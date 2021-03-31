---
description: La tabla FamilyFileRanges contiene información sobre determinados archivos de una imagen actualizada con intervalos que nunca deben sobrescribirse.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Tabla FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155524"
---
# <a name="familyfileranges-table-patchwizdll"></a>Tabla FamilyFileRanges (Patchwiz.dll)

La tabla FamilyFileRanges contiene información sobre determinados archivos de una imagen actualizada con intervalos que nunca deben sobrescribirse. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La tabla FamilyFileRanges tiene las columnas siguientes.



| Columna        | Tipo | Clave | Nullable |
|---------------|------|-----|----------|
| Familia        | text | Y   | N        |
| FTK           | text | Y   | N        |
| RetainOffsets | text |     | N        |
| RetainLengths | text |     | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia
</dt> <dd>

Clave externa para la columna Family de la [tabla ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave externa en las [tablas de archivos](file-table.md) de todas las imágenes actualizadas de la familia de imágenes.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Desplazamiento de los intervalos que no se pueden sobrescribir. El valor de este campo es una lista de los números de desplazamiento de intervalo para los intervalos que no se van a sobrescribir en los archivos de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainLengths.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths
</dt> <dd>

La longitud en bytes de los intervalos que no se pueden sobrescribir. El valor de este campo es una lista de números de longitud de intervalo para los intervalos que se conservan en los archivos de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainOffsets.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los desplazamientos y las longitudes especificados en RetainOffsets y RetainLengths no deben especificar intervalos superpuestos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



