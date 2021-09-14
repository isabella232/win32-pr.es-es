---
description: La tabla MsiPatchSequence contiene toda la información que requiere el instalador para determinar la secuencia de aplicación de una revisión de actualización pequeña con respecto a todas las demás revisiones.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabla MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169765"
---
# <a name="msipatchsequence-table"></a>Tabla MsiPatchSequence

La tabla MsiPatchSequence contiene toda la información que requiere el instalador para determinar la secuencia de aplicación de una revisión de actualización pequeña con respecto [a](small-updates.md) todas las demás revisiones. La tabla debe estar en la base de datos del archivo de revisión y no en una transformación de la revisión. El instalador omite esta tabla al aplicar una [revisión de actualización](major-upgrades.md) principal. Al aplicar una [revisión de actualización](minor-upgrades.md) secundaria, el instalador solo usa esta tabla para identificar las revisiones reemplazadas que no se deben secuenciar.

La **tabla MsiPatchSequence** tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| PatchFamily | [Identificador](identifier.md) | Y   | No        |
| ProductCode | [GUID](guid.md)             | Y   | Y        |
| Secuencia    | [Versión](version.md)       | No   | No        |
| Atributos  | [Entero](integer.md)       | No   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Especifica que la revisión es un miembro de la familia de revisiones denominada en este campo. Las revisiones de la misma familia de revisiones que tienen como destino la misma versión del producto se ordenan por los valores de la columna Secuencia. Las revisiones de la familia de revisiones se aplican al producto de destino en orden de aumento de la secuencia. PatchFamily también se usa para determinar qué revisiones se van a reemplazar. Una revisión puede aparecer en varias filas y pertenecer a varias familias de revisiones si se aplica a más de un producto o incluye varias correcciones.

El Windows instalador no interpreta el valor patchFamily de ninguna manera, aparte de las comparaciones de igualdad con otros valores de PatchFamily. Un valor PatchFamily debe ser único dentro del ProductCode de destino del conjunto de revisiones. En los escenarios de aplicación de revisiones complejos, es posible que el identificador patchFamily tenga que ser único globalmente.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>Productcode
</dt> <dd>

Un valor de este campo es opcional. Si [se](product-codes.md) especifica un GUID de código de producto en este campo y la revisión se aplica al producto especificado, la revisión se ordena y se aplica como miembro del patchFamily especificado. Si se especifica un GUID de código de producto en este campo y la revisión no se aplica al producto especificado por ProductCode, se omite esta fila. Si el valor de ProductCode es NULL, la revisión se ordena y se aplica como miembro de PatchFamily para todos los destinos de la revisión, independientemente del código del producto.

Una revisión puede tener varias filas en el mismo PatchFamily y un ProductCode diferente para cada producto al que se dirigirá la revisión. Una fila para PatchFamily puede especificar NULL para ProductCode. Si el producto de destino coincide con una fila con un ProductCode que no es NULL, el instalador usa la fila correspondiente y omite la fila con el código ProductCode NULL. Si ninguno de los códigos de producto especificados coincide con el destino, la revisión se ordena y se aplica como miembro de PatchFamily para todos los destinos de la revisión, independientemente del código del producto.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

El valor de la columna Secuencia especifica la secuencia de esta revisión dentro del patchFamily especificado. El valor de Sequence se expresa en el formato de datos [de](version.md) versión. El valor contiene entre 1 y 4 campos y cada campo tiene un intervalo de 0 a 65535. Los miembros de PatchFamily se ordenan y se aplican al producto de destino en el orden de aumento de los valores de secuencia. Por ejemplo, los seis valores siguientes aumentan: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

La presencia del atributo **msidbPatchSequenceSupersedeEarlier** en una [](small-updates.md) fila indica que la revisión de actualización pequeña reemplaza las actualizaciones proporcionadas por todas las revisiones con valores sequence menores en el mismo PatchFamily. Esta revisión contiene todas las correcciones proporcionadas por revisiones anteriores en el patchFamily especificado. Este atributo no significa que esta revisión sustituya a las revisiones anteriores en todos los casos porque las revisiones anteriores pueden pertenecer a varias familias de revisiones.

Una [revisión de](small-updates.md) actualización pequeña [](major-upgrades.md) no puede sustituir [una](minor-upgrades.md) actualización secundaria o una revisión de actualización principal en ninguna circunstancia, incluso si se establece **msidbPatchSequenceSupersedeEarlier.** 

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

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



