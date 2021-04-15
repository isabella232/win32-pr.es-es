---
description: La tabla MsiPatchSequence contiene toda la información que el instalador necesita para determinar la secuencia de aplicación de una revisión de actualización pequeña en relación con todas las demás revisiones.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabla MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669804"
---
# <a name="msipatchsequence-table"></a>Tabla MsiPatchSequence

La tabla MsiPatchSequence contiene toda la información que el instalador necesita para determinar la secuencia de aplicación de una revisión de [actualización pequeña](small-updates.md) en relación con todas las demás revisiones. La tabla debe estar en la base de datos del archivo de revisión y no en una transformación de la revisión. El instalador omite esta tabla al aplicar una revisión de [actualización principal](major-upgrades.md) . Al aplicar una revisión de [actualización secundaria](minor-upgrades.md) , el instalador solo usa esta tabla para identificar las revisiones reemplazadas que no se deben secuenciar.

La **tabla MsiPatchSequence** tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| PatchFamily | [Identificador](identifier.md) | Y   | N        |
| ProductCode | [GUID](guid.md)             | Y   | Y        |
| Secuencia    | [Versión](version.md)       | N   | N        |
| Atributos  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Especifica que la revisión es miembro de la familia de revisiones mencionada en este campo. Las revisiones de la misma familia de revisiones que tienen como destino la misma versión de producto se ordenan por los valores de la columna de secuencia. Las revisiones de la familia Patch se aplican al producto de destino en el orden de secuencia creciente. El PatchFamily también se usa para determinar qué revisiones se van a reemplazar. Una revisión puede aparecer en varias filas y pertenecer a varias familias de revisiones si se aplica a más de un producto o incluye varias correcciones.

El Windows Installer no interpreta el valor de PatchFamily de forma que no sea una comparación de igualdad con respecto a otros valores de PatchFamily. Un valor de PatchFamily debe ser único en la ProductCode de destino del conjunto de revisiones. En los escenarios de revisión complejos, es posible que el identificador PatchFamily tenga que ser único globalmente.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode
</dt> <dd>

Un valor de este campo es opcional. Si se especifica un GUID de [código de producto](product-codes.md) en este campo y la revisión se está aplicando al producto especificado, la revisión se ordenará y se aplicará como miembro del PatchFamily especificado. Si se especifica un GUID de código de producto en este campo y la revisión no se aplica al producto especificado por ProductCode, se omite esta fila. Si el valor de ProductCode es NULL, la revisión se ordena y se aplica como miembro de PatchFamily para todos los destinos de la revisión, independientemente del código de producto.

Una revisión puede tener varias filas en el mismo PatchFamily y un ProductCode diferente para cada producto de destino de la revisión. Una fila para PatchFamily puede especificar NULL para ProductCode. Si el producto de destino coincide con una fila con un valor ProductCode que no es NULL, el instalador usa la fila coincidente y omite la fila con el valor ProductCode nulo. Si ninguno de los códigos de producto especificados coincide con el destino, la revisión se ordena y se aplica como miembro de PatchFamily para todos los destinos de la revisión, independientemente del código de producto.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ
</dt> <dd>

El valor de la columna Sequence especifica la secuencia de esta revisión en el PatchFamily especificado. El valor de Sequence se expresa en el formato de los datos de la [versión](version.md) . El valor contiene entre 1 y 4 campos y cada campo tiene un intervalo de 0 a 65535. Los miembros de PatchFamily se ordenan y se aplican al producto de destino en el orden en que los valores de secuencia aumentan. Por ejemplo, los seis valores siguientes aumentan: 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

La presencia del atributo **msidbPatchSequenceSupersedeEarlier** en una fila indica que la revisión de [actualización pequeña](small-updates.md) sustituye las actualizaciones proporcionadas por todas las revisiones con valores de secuencia inferiores en el mismo PatchFamily. Esta revisión contiene todas las revisiones proporcionadas por las revisiones anteriores en el PatchFamily especificado. Este atributo no significa que esta revisión sustituya a las revisiones anteriores en todos los casos, ya que las revisiones anteriores pueden pertenecer a varias familias de revisiones.

Una revisión de [actualización pequeña](small-updates.md) no puede sustituir una [actualización secundaria](minor-upgrades.md) o una revisión de [actualización importante](major-upgrades.md) en cualquier circunstancia, incluso si se establece **msidbPatchSequenceSupersedeEarlier** . 

| Nombre                                   | Value | Significado                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | Indica un valor de secuenciación simple.                              |
| **msidbPatchSequenceSupersedeEarlier** | 0x01  | Indica una revisión que sustituye a las revisiones anteriores de esta familia. |



 

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



