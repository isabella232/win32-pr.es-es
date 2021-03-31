---
description: La tabla MsiPatchOldAssemblyName especifica el nombre anterior de un ensamblado.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Tabla MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361068"
---
# <a name="msipatcholdassemblyname-table"></a>Tabla MsiPatchOldAssemblyName

La tabla MsiPatchOldAssemblyName especifica el nombre anterior de un ensamblado.

La tabla MsiPatchOldAssemblyName tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Ensamblado | [Identificador](identifier.md) | Y   | N        |
| Nombre     | [Texto](text.md)             | Y   | N        |
| Value    | [Texto](text.md)             | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembl
</dt> <dd>

Identificador único del nombre del ensamblado antiguo. Esta clave se usa como una asignación entre esta y la [tabla MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Nombre del atributo asociado con el valor especificado en la columna valor.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor asociado al nombre especificado en la columna nombre.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Windows Installer usa la tabla [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla MsiPatchOldAssemblyName al aplicar revisiones a los ensamblados instalados en la caché de ensamblados global (GAC). Al liberar una versión más reciente de un ensamblado, se cambia el nombre seguro del ensamblado. Las dos tablas juntas identifican el nombre anterior del ensamblado de un ensamblado actualizado. Esto permite al instalador usar el nombre de ensamblado anterior para buscar el archivo original en la GAC y aplicar una revisión binaria. Sin esta información, es posible que el instalador tenga que obtener acceso al origen de instalación original con el fin de aplicar una revisión a un ensamblado instalado en la GAC.

[PatchWiz](patchwiz-dll.md)no genera automáticamente la tabla [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla MsiPatchOldAssemblyName. El paquete de actualización especificado en la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md) debe contener estas tablas para que la revisión tenga esta información.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



