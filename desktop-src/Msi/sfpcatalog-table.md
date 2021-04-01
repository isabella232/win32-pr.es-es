---
description: La tabla SFPCatalog contiene los catálogos que usa Windows me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Tabla SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275664"
---
# <a name="sfpcatalog-table"></a>Tabla SFPCatalog

La tabla SFPCatalog contiene los catálogos que usa Windows me.

La tabla SFPCatalog tiene las columnas siguientes.



| Columna     | Tipo                       | Clave | Nullable |
|------------|----------------------------|-----|----------|
| SFPCatalog | [Nombre de archivo](filename.md)   | Y   | N        |
| Catálogo    | [Binario](binary.md)       | N   | N        |
| Dependencia | [Formatea](formatted.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog
</dt> <dd>

Nombre corto de archivo para el catálogo. Dado que los catálogos no tienen ninguna versión, el catálogo especificado en esta columna puede sobrescribir un catálogo que tenga el mismo nombre y ya esté instalado en el sistema local. Vea el tema sobre el control de versiones de archivos. el [archivo tiene una versión](neither-file-has-a-version.md).

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo
</dt> <dd>

Datos binarios para el catálogo.

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Pendiente
</dt> <dd>

El catálogo especificado en este campo es el elemento primario del catálogo dependiente especificado en el campo SFPCatalog. Escriba el nombre corto de archivo del catálogo primario en el campo dependencia. Este campo es una clave de vuelta a la columna SFPCatalog. La coincidencia de dependencia distingue mayúsculas de minúsculas.

Si el campo de dependencia hace referencia a otro registro de esta tabla SFPCatalog, el catálogo primario se instala antes que el catálogo dependiente.

Si el campo de dependencia hace referencia a un catálogo primario que no está presente en el campo SFPCatalog de esta tabla y si el catálogo primario no está ya instalado, se produce un error en la instalación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [acción InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta la tabla de [componentes](component-table.md), la tabla de [archivos](file-table.md), la tabla [FileSFPCatalog](filesfpcatalog-table.md) y la tabla SFPCatalog.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



