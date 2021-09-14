---
description: En la tabla ODBCTranslator se enumeran los traductores ODBC que pertenecen a la instalación.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Tabla ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251060"
---
# <a name="odbctranslator-table"></a>Tabla ODBCTranslator

En la tabla ODBCTranslator se enumeran los traductores ODBC que pertenecen a la instalación.

La tabla ODBCTranslator tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Translator  | [Identificador](identifier.md) | Y   | No        |
| Componente\_ | [Identificador](identifier.md) | No   | No        |
| Descripción | [Texto](text.md)             | No   | No        |
| Archivo\_      | [Identificador](identifier.md) | No   | No        |
| Instalación de \_ archivos | [Identificador](identifier.md) | No   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Traductor
</dt> <dd>

Nombre de token interno para traductor. Clave principal de la tabla.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la tabla Component.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción registrada para este traductor de controladores ODBC. Este valor no se puede localizar.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Archivo DLL para la transferencia que aparece en la Traductor columna. La columna \_ Archivo es una clave externa en la tabla [File](file-table.md). El nombre de archivo especificado en la columna Nombre de archivo de ese registro de tabla de archivos debe tener el formato de nombre de archivo corto. No se puede \| usar la sintaxis LFN de SFN.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Instalación de \_ archivos
</dt> <dd>

Archivo DLL de instalación para el traductor si es diferente de la columna Traductor configuración. La columna \_ Archivo es una clave externa en la tabla [File](file-table.md). El nombre de archivo especificado en la columna Nombre de archivo de ese registro de tabla de archivos debe tener el formato de nombre de archivo corto. No se puede \| usar la sintaxis LFN de SFN.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las [acciones InstallODBC](installodbc-action.md) [y RemoveODBC](removeodbc-action.md) de las tablas [*de*](s-gly.md) secuencia procesan la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



