---
description: En la tabla ODBCDriver se enumeran los controladores ODBC que pertenecen a la instalación.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabla ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eb0da3217d7466fc0beef90933c8a6af32e3d0551ecc6975a31ac55ed2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943126"
---
# <a name="odbcdriver-table"></a>Tabla ODBCDriver

En la tabla ODBCDriver se enumeran los controladores ODBC que pertenecen a la instalación.

La tabla ODBCDriver tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Controlador      | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |
| Descripción | [Texto](text.md)             | N   | N        |
| Archivo\_      | [Identificador](identifier.md) | N   | N        |
| Instalación de \_ archivos | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Conductor
</dt> <dd>

Nombre del token interno para el controlador. Una clave principal para la tabla

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la tabla Component.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción registrada para este controlador ODBC. Este valor no se puede localizar.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Archivo DLL para los controladores enumerados en la columna Controlador. La columna \_ Archivo es una clave externa en la tabla [File](file-table.md). El nombre de archivo especificado en la columna Nombre de archivo de ese registro de tabla de archivos debe tener el formato de nombre de archivo corto. No se puede \| usar la sintaxis LFN de SFN.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Instalación de \_ archivos
</dt> <dd>

Archivo DLL de instalación para el controlador si es diferente del controlador. La columna \_ Archivo es una clave externa en la tabla [File](file-table.md). El nombre de archivo especificado en la columna Nombre de archivo de ese registro de tabla de archivos debe tener el formato de nombre de archivo corto. No se puede \| usar la sintaxis LFN de SFN.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las [acciones InstallODBC](installodbc-action.md) [y RemoveODBC](removeodbc-action.md) de las tablas [*de*](s-gly.md) secuencia procesan la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



