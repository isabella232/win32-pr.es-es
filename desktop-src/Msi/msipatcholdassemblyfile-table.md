---
description: La tabla MsiPatchOldAssemblyFile relaciona un archivo de la tabla File con un nombre de ensamblado de la tabla MsiPatchOldAssemblyName. Se pueden asociar varios nombres de ensamblado antiguos a un solo archivo.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabla MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4570b862773d2dc1d5b9c7458dbc1ccd8825ce77bf504d5e0fb2bf116d7a095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559085"
---
# <a name="msipatcholdassemblyfile-table"></a>Tabla MsiPatchOldAssemblyFile

La tabla MsiPatchOldAssemblyFile relaciona un archivo de la tabla [File](file-table.md) con un nombre de ensamblado de la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md). Se pueden asociar varios nombres de ensamblado antiguos a un solo archivo.

La tabla MsiPatchOldAssemblyFile tiene las siguientes columnas.



| Columna     | Tipo                         | Clave | Nullable |
|------------|------------------------------|-----|----------|
| Archivo\_     | [Identificador](identifier.md) | Y   | N        |
| Ensamblado\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Clave externa a la [tabla File](file-table.md) que especifica el ensamblado al que se va a aplicar la revisión. Esta columna forma parte de la clave principal.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>ensamblaje\_
</dt> <dd>

Clave externa de la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) que identifica uno de los nombres de ensamblado antiguos para el ensamblado. Esta columna forma parte de la clave principal.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Windows El instalador usa la tabla MsiPatchOldAssemblyFile y la tabla [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) al aplicar revisiones a los ensamblados instalados en la caché global de ensamblados (GAC). Al publicar una versión más reciente de un ensamblado, se cambia el nombre fuerte del ensamblado. Las dos tablas juntos identifican el nombre de ensamblado antiguo de un ensamblado actualizado. Esto permite al instalador usar el nombre de ensamblado antiguo para buscar el archivo original en la GAC y aplicar una revisión binaria. Sin esta información, es posible que el instalador tenga que acceder al origen de instalación original para aplicar revisiones a un ensamblado instalado en la GAC.

[PatchWiz](patchwiz-dll.md)no genera automáticamente la tabla MsiPatchOldAssemblyFile y la tabla [MsiPatchOldAssemblyName.](msipatcholdassemblyname-table.md) El paquete de actualización especificado en la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md) debe contener estas tablas para que la revisión tenga esta información.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



