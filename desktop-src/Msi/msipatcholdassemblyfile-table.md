---
description: La tabla MsiPatchOldAssemblyFile relaciona un archivo de la tabla File con un nombre de ensamblado de la tabla MsiPatchOldAssemblyName. Se pueden asociar varios nombres de ensamblado antiguos a un único archivo.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabla MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169786"
---
# <a name="msipatcholdassemblyfile-table"></a>Tabla MsiPatchOldAssemblyFile

La tabla MsiPatchOldAssemblyFile relaciona un archivo de la tabla [File](file-table.md) con un nombre de ensamblado de la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md). Se pueden asociar varios nombres de ensamblado antiguos a un único archivo.

La tabla MsiPatchOldAssemblyFile tiene las columnas siguientes.



| Columna     | Tipo                         | Clave | Nullable |
|------------|------------------------------|-----|----------|
| Archivo\_     | [Identificador](identifier.md) | Y   | No        |
| Ensamblado\_ | [Identificador](identifier.md) | Y   | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Clave externa a la [tabla File](file-table.md) que especifica el ensamblado al que se va a aplicar la revisión. Esta columna forma parte de la clave principal.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Ensamblaje\_
</dt> <dd>

Clave externa de la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) que identifica uno de los nombres de ensamblado antiguos para el ensamblado. Esta columna forma parte de la clave principal.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Windows El instalador usa la tabla MsiPatchOldAssemblyFile y la tabla [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) al aplicar revisiones a los ensamblados instalados en la caché global de ensamblados (GAC). Al publicar una versión más reciente de un ensamblado, se cambia el nombre fuerte del ensamblado. Las dos tablas juntos identifican el nombre de ensamblado antiguo de un ensamblado actualizado. Esto permite al instalador usar el nombre de ensamblado antiguo para buscar el archivo original en la GAC y aplicar una revisión binaria. Sin esta información, es posible que el instalador tenga que acceder al origen de instalación original para aplicar revisiones a un ensamblado instalado en la GAC.

[PatchWiz](patchwiz-dll.md)no genera automáticamente la tabla MsiPatchOldAssemblyFile y la tabla [MsiPatchOldAssemblyName.](msipatcholdassemblyname-table.md) El paquete de actualización especificado en la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md) debe contener estas tablas para que la revisión tenga esta información.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



