---
description: La tabla ODBCAttribute contiene información sobre los atributos de los controladores y traductores ODBC (Conectividad abierta de bases de datos).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Tabla ODBCAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155132"
---
# <a name="odbcattribute-table"></a>Tabla ODBCAttribute

La tabla ODBCAttribute contiene información sobre los atributos de los controladores y traductores ODBC (Conectividad abierta de bases de datos).

La tabla ODBCAttribute tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Controlador\_  | [Identificador](identifier.md) | Y   | N        |
| Atributo | [Texto](text.md)             | Y   | N        |
| Value     | [Formatea](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Dispositivo\_
</dt> <dd>

Nombre del token interno para un controlador. Clave principal de la tabla. Una clave externa en la [tabla ODBCDriver](odbcdriver-table.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atribui
</dt> <dd>

Nombre del atributo de controlador. Clave principal de la tabla.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de cadena localizable para el atributo.

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

 

 



