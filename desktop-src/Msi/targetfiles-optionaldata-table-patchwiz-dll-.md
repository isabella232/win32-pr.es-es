---
description: La \_ tabla TargetFiles OptionalData contiene información sobre los archivos específicos de una imagen de destino. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: Tabla TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002362"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>TargetFiles \_ OptionalData (Patchwiz.dll)

La \_ tabla TargetFiles OptionalData contiene información sobre los archivos específicos de una imagen de destino. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La \_ tabla TargetFiles OptionalData tiene las columnas siguientes.



| Columna        | Tipo | Clave | Nullable |
|---------------|------|-----|----------|
| Destino        | text | Y   | N        |
| FTK           | text | Y   | N        |
| SymbolPaths   | text |     | Y        |
| IgnoreOffsets | text |     | Y        |
| IgnoreLengths | text |     | Y        |
| RetainOffsets | text |     | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir
</dt> <dd>

Clave externa para la columna de destino de la [tabla TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave externa en la [tabla de archivos](file-table.md) de la imagen de destino.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

El valor de este campo se agrega a la lista de carpetas delimitada por punto y coma de la columna SymbolPaths de la [tabla TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) cuando se genera la revisión, y se puede usar para agregar archivos de símbolos para un archivo específico.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a omitir en el archivo de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreLengths. Esta columna es opcional.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

El valor de este campo es una lista delimitada por comas de longitudes de intervalo en bytes para los intervalos que se van a omitir en el archivo de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreOffsets. Esta columna es opcional.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a conservar en el archivo de destino. El orden y el número de los intervalos de la lista debe coincidir con los elementos de la columna RetainOffsets del registro correspondiente en la [tabla FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



