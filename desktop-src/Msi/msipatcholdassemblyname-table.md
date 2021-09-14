---
description: La tabla MsiPatchOldAssemblyName especifica el nombre antiguo de un ensamblado.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Tabla MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169781"
---
# <a name="msipatcholdassemblyname-table"></a>Tabla MsiPatchOldAssemblyName

La tabla MsiPatchOldAssemblyName especifica el nombre antiguo de un ensamblado.

La tabla MsiPatchOldAssemblyName tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Ensamblado | [Identificador](identifier.md) | Y   | No        |
| Nombre     | [Texto](text.md)             | Y   | No        |
| Value    | [Texto](text.md)             | No   | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Ensamblaje
</dt> <dd>

Identificador único para el nombre de ensamblado antiguo. Esta clave se usa como asignación entre este y la [tabla MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre del atributo asociado al valor especificado en la columna Valor .

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor asociado al nombre especificado en la columna Nombre.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Windows El instalador usa [la tabla MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla MsiPatchOldAssemblyName al aplicar revisiones a los ensamblados instalados en la caché global de ensamblados (GAC). Al liberar una versión más reciente de un ensamblado, se cambia el nombre de seguridad del ensamblado. Las dos tablas juntos identifican el nombre de ensamblado antiguo para un ensamblado actualizado. Esto permite al instalador usar el nombre de ensamblado anterior para buscar el archivo original en la GAC y aplicar una revisión binaria. Sin esta información, es posible que el instalador tenga que acceder al origen de instalación original para aplicar revisiones a un ensamblado instalado en la GAC.

[PatchWiz](patchwiz-dll.md)no genera automáticamente la tabla [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla MsiPatchOldAssemblyName. El paquete de actualización especificado en la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md) debe contener estas tablas para que la revisión tenga esta información.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



