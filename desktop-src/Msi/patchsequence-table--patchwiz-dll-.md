---
description: La tabla PatchSequence se usa para generar la tabla MsiPatchSequence en una revisión. La tabla requiere la versión de PATCHWIZ.DLL que está disponible con Windows Installer&\# 160; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Tabla PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913465"
---
# <a name="patchsequence-table-patchwizdll"></a>Tabla PatchSequence (PATCHWIZ.DLL)

La tabla PatchSequence se usa para generar la [tabla MsiPatchSequence](msipatchsequence-table.md) en una revisión. La tabla requiere la versión de [PATCHWIZ.DLL](patchwiz-dll.md) que está disponible con Windows Installer 3,0.

En la tabla siguiente se identifican las columnas de la tabla PatchSequence.



| Columna      | Tipo       | Clave | Nullable |
|-------------|------------|-----|----------|
| PatchFamily | Identificador | Y   | N        |
| Destino      | Texto       | Y   | Y        |
| Secuencia    | Versión    |     | Y        |
| Sustituir   | Entero    |     | Y        |



 

### <a name="columns"></a>Columnas

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

El identificador que indica las familias de secuencias a las que pertenece esta revisión.

Los valores de las columnas target y PatchFamily definen conjuntamente la clave principal de la tabla. Una revisión que pertenece a varias familias de secuencias, o tiene secuencias diferentes según el código de producto del destino, puede tener una fila por cada emparejamiento. Este valor se usa para rellenar la columna PatchFamily de la [tabla MsiPatchSequence](msipatchsequence-table.md) que pertenece a la revisión.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir
</dt> <dd>

La columna de destino se usa para filtrar el PatchFamily por el código de producto.

Un valor NULL en esta columna indica que este PatchFamily se aplica a todos los destinos de la revisión. Si esta columna contiene una clave externa para la [tabla TargetImages](targetimages-table-patchwiz-dll-.md), el código de producto de la imagen especificada se recupera y se usa para rellenar el valor del código de producto en la fila de la nueva revisión de la [tabla MsiPatchSequence](msipatchsequence-table.md). Si esta columna contiene un GUID, el GUID se usa para rellenar el valor de código de producto de la fila en la tabla MsiPatchSequence.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ
</dt> <dd>

El valor de la columna Sequence se usa para rellenar la columna Sequence de la [tabla MsiPatchSequence](msipatchsequence-table.md) del nuevo archivo de revisión.

Si el valor es NULL, se genera automáticamente un número de secuencia.

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Sustituir
</dt> <dd>

Un valor de **msidbPatchSequenceSupersedeEarlier** o 1 en este campo indica que esta revisión sustituye a [las actualizaciones pequeñas](small-updates.md) anteriores de las familias de secuencias a las que pertenece esta revisión.

El valor de esta columna se utiliza para establecer la columna de atributos de la fila de la nueva revisión en la [tabla MsiPatchSequence](msipatchsequence-table.md) .

</dd> </dl>

### <a name="remarks"></a>Observaciones

Disponible a partir de Windows Installer 3,0.

 

 



