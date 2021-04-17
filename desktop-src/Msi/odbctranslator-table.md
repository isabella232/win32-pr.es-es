---
description: En la tabla ODBCTranslator se enumeran los traductores ODBC que pertenecen a la instalación de.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Tabla ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653055"
---
# <a name="odbctranslator-table"></a>Tabla ODBCTranslator

En la tabla ODBCTranslator se enumeran los traductores ODBC que pertenecen a la instalación de.

La tabla ODBCTranslator tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Translator  | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |
| Descripción | [Texto](text.md)             | N   | N        |
| Archivo\_      | [Identificador](identifier.md) | N   | N        |
| Configuración de archivos \_ | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator
</dt> <dd>

Nombre del token interno para Translator. Clave principal de la tabla.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la tabla de componentes.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Descripción registrada para este traductor de controladores ODBC. Este valor no se puede localizar.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

El archivo DLL para la transferencia que se muestra en la columna Translator. La columna de archivo \_ es una clave externa de la [tabla de archivos](file-table.md). El nombre de archivo especificado en la columna FILENAME de ese registro de tabla de archivos debe estar en el formato de nombre de archivo corto. No se \| puede usar la sintaxis de LFN de SFN.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuración de archivos \_
</dt> <dd>

El archivo DLL de instalación del traductor si es diferente de la columna Translator. La columna de archivo \_ es una clave externa de la [tabla de archivos](file-table.md). El nombre de archivo especificado en la columna FILENAME de ese registro de tabla de archivos debe estar en el formato de nombre de archivo corto. No se \| puede usar la sintaxis de LFN de SFN.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones [InstallODBC](installodbc-action.md) y [RemoveODBC](removeodbc-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



