---
description: La tabla PatchSequence se usa para generar la tabla MsiPatchSequence en una revisión. La tabla requiere la versión de PATCHWIZ.DLL que está disponible con Windows Installer&\# 160;3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Tabla PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0281f9882a674b268466259c534eefaa468bacf0fa891dc3a385e4d580a1e8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129185"
---
# <a name="patchsequence-table-patchwizdll"></a>Tabla PatchSequence (PATCHWIZ.DLL)

La tabla PatchSequence se usa para generar [la tabla MsiPatchSequence](msipatchsequence-table.md) en una revisión. La tabla requiere la versión de [PATCHWIZ.DLL](patchwiz-dll.md) que está disponible con Windows Installer 3.0.

En la tabla siguiente se identifican las columnas de la tabla PatchSequence.



| Columna      | Tipo       | Clave | Nullable |
|-------------|------------|-----|----------|
| PatchFamily | Identificador | Y   | N        |
| Destino      | Texto       | Y   | Y        |
| Secuencia    | Versión    |     | Y        |
| Reemplazar   | Entero    |     | Y        |



 

### <a name="columns"></a>Columnas

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Identificador que indica las familias de secuencias a las que pertenece esta revisión.

Los valores de las columnas Target y PatchFamily juntos definen la clave principal de la tabla. Una revisión que pertenezca a varias familias de secuencias, o que tenga secuencias diferentes en función del código de producto del destino, puede tener una fila para cada emparejamiento. Este valor se usa para rellenar la columna PatchFamily de [la tabla MsiPatchSequence](msipatchsequence-table.md) que pertenece a la revisión.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Objetivo
</dt> <dd>

La columna Destino se usa para filtrar PatchFamily por código de producto.

Un valor NULL de esta columna indica que patchFamily se aplica a todos los destinos de la revisión. Si esta columna contiene una clave externa para la tabla [TargetImages](targetimages-table-patchwiz-dll-.md), se recupera el código de producto de la imagen especificada y se usa para rellenar el valor del código de producto en la fila de la nueva revisión de la tabla [MsiPatchSequence](msipatchsequence-table.md). Si esta columna contiene un GUID, el GUID se usa para rellenar el valor del código de producto de la fila en la tabla MsiPatchSequence.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

El valor de la columna Sequence se usa para rellenar la columna Sequence de [la tabla MsiPatchSequence](msipatchsequence-table.md) del nuevo archivo de revisión.

Si el valor es NULL, se genera automáticamente un número de secuencia.

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Reemplazar
</dt> <dd>

Un valor de **msidbPatchSequenceSupersedeEarlier** o 1 en este campo [](small-updates.md) indica que esta revisión reemplaza a las actualizaciones pequeñas anteriores en las familias de secuencias a las que pertenece esta revisión.

El valor de esta columna se usa para establecer la columna Atributos de la fila de la nueva revisión en [la tabla MsiPatchSequence](msipatchsequence-table.md) .

</dd> </dl>

### <a name="remarks"></a>Comentarios

Disponible a partir de Windows Installer 3.0.

 

 



