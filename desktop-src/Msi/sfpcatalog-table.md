---
description: La tabla SFPCatalog contiene los catálogos usados por Windows Me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Tabla SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97498ff6437967a4a588be7b957aea130dad201699d55fad3abace6ff094b271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624896"
---
# <a name="sfpcatalog-table"></a>Tabla SFPCatalog

La tabla SFPCatalog contiene los catálogos usados por Windows Me.

La tabla SFPCatalog tiene las siguientes columnas.



| Columna     | Tipo                       | Key | Nullable |
|------------|----------------------------|-----|----------|
| SFPCatalog | [Nombre de archivo](filename.md)   | Y   | N        |
| Catálogo    | [Binario](binary.md)       | N   | N        |
| Dependencia | [Formato](formatted.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog
</dt> <dd>

Nombre de archivo corto del catálogo. Dado que los catálogos no tienen ninguna versión, el catálogo especificado en esta columna puede sobrescribir un catálogo que tenga el mismo nombre y ya esté instalado en el sistema local. Vea el tema de control de versiones de [archivos Ninguno de los archivos tiene una versión](neither-file-has-a-version.md).

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo
</dt> <dd>

Datos binarios del catálogo.

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependencia
</dt> <dd>

El catálogo especificado en este campo es el elemento primario del catálogo dependiente especificado en el campo SFPCatalog. Escriba el nombre de archivo corto del catálogo primario en el campo Dependencia. Este campo es una clave de nuevo en la columna SFPCatalog. La coincidencia de dependencia distingue mayúsculas de minúsculas.

Si el campo Dependencia hace referencia a otro registro de esta tabla SFPCatalog, el catálogo primario se instala antes que el catálogo dependiente.

Si el campo Dependencia hace referencia a un catálogo primario que no está presente en el campo SFPCatalog de esta tabla y si el catálogo primario aún no está instalado, se produce un error en la instalación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [acción InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta la tabla [Component](component-table.md), la [tabla File,](file-table.md) [la tabla FileSFPCatalog](filesfpcatalog-table.md) y la tabla SFPCatalog.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



