---
description: La tabla TargetFiles \_ OptionalData contiene información sobre archivos específicos de una imagen de destino. Esta tabla es opcional en la base de datos de creación de revisiones (archivo .fp) y la usa la función UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: TargetFiles_OptionalData tabla (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069616"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>TargetFiles \_ OptionalData Table (Patchwiz.dll)

La tabla TargetFiles \_ OptionalData contiene información sobre archivos específicos de una imagen de destino. Esta tabla es opcional en la base de datos de creación de revisiones (archivo .fp) y la usa la función [UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabla TargetFiles \_ OptionalData tiene las siguientes columnas.



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

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Objetivo
</dt> <dd>

Clave externa a la columna Target de [la tabla TargetImages (Patchwiz.dll).](targetimages-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Clave externa en la [tabla Archivo de](file-table.md) la imagen de destino.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

El valor de este campo se agrega a la lista delimitada por punto y coma de carpetas en la columna SymbolPaths de la tabla [TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) cuando se genera la revisión y se puede usar para agregar archivos de símbolos para un archivo específico.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a omitir en el archivo de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreLengths. Esta columna es opcional.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirán los valores en ULONG.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

El valor de este campo es una lista delimitada por comas de longitudes de intervalo en bytes para los intervalos que se van a omitir en el archivo de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreOffsets. Esta columna es opcional.

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirán los valores en ULONG.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se conservarán en el archivo de destino. El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainOffsets del registro correspondiente de la [tabla FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)

Los valores pueden ser decimales o hexadecimales. [Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena y Patchwiz.dll convertirán los valores en ULONG.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



