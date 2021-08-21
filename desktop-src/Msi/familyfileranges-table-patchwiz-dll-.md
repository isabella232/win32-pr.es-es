---
description: La tabla FamilyFileRanges contiene información sobre archivos concretos de una imagen actualizada con intervalos que nunca se deben sobrescribir.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Tabla FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0559f4cea1061f9cf0c1438140e7abba8b00908233a1a1d608ae5dbd8b79ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636902"
---
# <a name="familyfileranges-table-patchwizdll"></a>Tabla FamilyFileRanges (Patchwiz.dll)

La tabla FamilyFileRanges contiene información sobre archivos concretos de una imagen actualizada con intervalos que nunca se deben sobrescribir. Esta tabla es opcional en la base de datos de creación de revisiones (archivo .fp) y la usa la función [UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabla FamilyFileRanges tiene las columnas siguientes.



| Columna        | Tipo | Clave | Nullable |
|---------------|------|-----|----------|
| Familia        | texto | Y   | N        |
| FTK           | texto | Y   | N        |
| RetainOffsets | texto |     | N        |
| RetainLengths | texto |     | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia
</dt> <dd>

Clave externa a la columna Familia de [la tabla ImageFamilies (Patchwiz.dll).](imagefamilies-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave externa en las [tablas file de](file-table.md) todas las imágenes actualizadas de la familia de imágenes.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Desplazamiento de los intervalos que no se pueden sobrescribir. El valor de este campo es una lista de los números de desplazamiento de intervalo para los intervalos que no se van a sobrescribir en los archivos de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainLengths.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONG.

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths
</dt> <dd>

Longitud en bytes de los intervalos que no se pueden sobrescribir. El valor de este campo es una lista de números de longitud de intervalo para los intervalos que se conservarán en los archivos de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainOffsets.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONG.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los desplazamientos y longitudes especificados en RetainOffsets y RetainLengths no deben especificar intervalos superpuestos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



