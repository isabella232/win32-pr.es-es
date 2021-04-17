---
description: La tabla MsiPatchOldAssemblyFile relaciona un archivo de la tabla de archivos con un nombre de ensamblado de la tabla MsiPatchOldAssemblyName. Se pueden asociar varios nombres de ensamblado anteriores a un único archivo.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabla MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669845"
---
# <a name="msipatcholdassemblyfile-table"></a>Tabla MsiPatchOldAssemblyFile

La tabla MsiPatchOldAssemblyFile relaciona un archivo de la tabla de [archivos](file-table.md) con un nombre de ensamblado de la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md). Se pueden asociar varios nombres de ensamblado anteriores a un único archivo.

La tabla MsiPatchOldAssemblyFile tiene las columnas siguientes.



| Columna     | Tipo                         | Clave | Nullable |
|------------|------------------------------|-----|----------|
| Archivo\_     | [Identificador](identifier.md) | Y   | N        |
| Assembl\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

Clave externa de la [tabla de archivos](file-table.md) que especifica el ensamblado que se va a revisar. Esta columna forma parte de la clave principal.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembl\_
</dt> <dd>

Clave externa de la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) que identifica uno de los nombres de ensamblado anteriores para el ensamblado. Esta columna forma parte de la clave principal.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Windows Installer usa la tabla MsiPatchOldAssemblyFile y la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) al aplicar revisiones a los ensamblados instalados en la caché de ensamblados global (GAC). Al liberar una versión más reciente de un ensamblado, se cambia el nombre seguro del ensamblado. Las dos tablas juntas identifican el nombre anterior del ensamblado de un ensamblado actualizado. Esto permite al instalador usar el nombre de ensamblado anterior para buscar el archivo original en la GAC y aplicar una revisión binaria. Sin esta información, es posible que el instalador tenga que obtener acceso al origen de instalación original con el fin de aplicar una revisión a un ensamblado instalado en la GAC.

[PatchWiz](patchwiz-dll.md)no genera automáticamente la tabla MsiPatchOldAssemblyFile y la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) . El paquete de actualización especificado en la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md) debe contener estas tablas para que la revisión tenga esta información.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



