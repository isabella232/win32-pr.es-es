---
description: La tabla MsiPatchOldAssemblyName especifica el nombre antiguo de un ensamblado.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Tabla MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d8f5a57d0b4ec90687f19a995dfc794e3a75cccbd21fd3bdcd2eef5ae4645f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519815"
---
# <a name="msipatcholdassemblyname-table"></a>Tabla MsiPatchOldAssemblyName

La tabla MsiPatchOldAssemblyName especifica el nombre antiguo de un ensamblado.

La tabla MsiPatchOldAssemblyName tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Ensamblado | [Identificador](identifier.md) | Y   | N        |
| Nombre     | [Texto](text.md)             | Y   | N        |
| Value    | [Texto](text.md)             | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>ensamblaje
</dt> <dd>

Identificador único del nombre del ensamblado anterior. Esta clave se usa como asignación entre this y la [tabla MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre del atributo asociado al valor especificado en la columna Valor.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor asociado al nombre especificado en la columna Nombre.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Windows El instalador usa [la tabla MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla MsiPatchOldAssemblyName al aplicar revisiones a los ensamblados instalados en la caché global de ensamblados (GAC). Al publicar una versión más reciente de un ensamblado, se cambia el nombre fuerte del ensamblado. Las dos tablas juntos identifican el nombre de ensamblado antiguo de un ensamblado actualizado. Esto permite al instalador usar el nombre de ensamblado antiguo para buscar el archivo original en la GAC y aplicar una revisión binaria. Sin esta información, es posible que el instalador tenga que acceder al origen de instalación original para aplicar revisiones a un ensamblado instalado en la GAC.

[PatchWiz](patchwiz-dll.md)no genera automáticamente la tabla [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla MsiPatchOldAssemblyName. El paquete de actualización especificado en la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md) debe contener estas tablas para que la revisión tenga esta información.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



