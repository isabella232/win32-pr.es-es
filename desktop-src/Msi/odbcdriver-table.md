---
description: En la tabla ODBCDriver se muestran los controladores ODBC que pertenecen a la instalación de.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabla ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541067"
---
# <a name="odbcdriver-table"></a>Tabla ODBCDriver

En la tabla ODBCDriver se muestran los controladores ODBC que pertenecen a la instalación de.

La tabla ODBCDriver tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Controlador      | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |
| Descripción | [Texto](text.md)             | N   | N        |
| Archivo\_      | [Identificador](identifier.md) | N   | N        |
| Configuración de archivos \_ | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Dispositivo
</dt> <dd>

Nombre del token interno del controlador. Una clave principal para la tabla

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la tabla de componentes.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

La descripción registrada para este controlador ODBC. Este valor no se puede localizar.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

El archivo DLL para los controladores enumerados en la columna controlador. La columna de archivo \_ es una clave externa de la [tabla de archivos](file-table.md). El nombre de archivo especificado en la columna FILENAME de ese registro de tabla de archivos debe estar en el formato de nombre de archivo corto. No se \| puede usar la sintaxis de LFN de SFN.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuración de archivos \_
</dt> <dd>

El archivo DLL de instalación del controlador si es diferente del controlador. La columna de archivo \_ es una clave externa de la [tabla de archivos](file-table.md). El nombre de archivo especificado en la columna FILENAME de ese registro de tabla de archivos debe estar en el formato de nombre de archivo corto. No se \| puede usar la sintaxis de LFN de SFN.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones [InstallODBC](installodbc-action.md) y [RemoveODBC](removeodbc-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



