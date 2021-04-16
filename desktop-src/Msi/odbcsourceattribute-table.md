---
description: La tabla ODBCSourceAttribute contiene información sobre los atributos de los orígenes de datos.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Tabla ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541054"
---
# <a name="odbcsourceattribute-table"></a>Tabla ODBCSourceAttribute

La tabla ODBCSourceAttribute contiene información sobre los atributos de los orígenes de datos.

La tabla ODBCSourceAttribute tiene las columnas siguientes.



| Columna       | Tipo                         | Clave | Nullable |
|--------------|------------------------------|-----|----------|
| DataSource\_ | [Identificador](identifier.md) | Y   | N        |
| Atributo    | [Texto](text.md)             | Y   | N        |
| Value        | [Formatea](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_
</dt> <dd>

Nombre del token interno para el origen de datos. Clave principal de la tabla.

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atribui
</dt> <dd>

Nombre del atributo de origen de datos. Clave principal de la tabla.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de cadena traducible para el atributo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones [InstallODBC](installodbc-action.md) y [RemoveODBC](removeodbc-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



