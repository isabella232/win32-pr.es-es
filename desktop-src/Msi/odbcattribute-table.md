---
description: La tabla ODBCAttribute contiene información sobre los atributos de los controladores y traductores de Open Database Connectivity (ODBC).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Tabla ODBCAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251073"
---
# <a name="odbcattribute-table"></a>Tabla ODBCAttribute

La tabla ODBCAttribute contiene información sobre los atributos de los controladores y traductores de Open Database Connectivity (ODBC).

La tabla ODBCAttribute tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Conductor\_  | [Identificador](identifier.md) | Y   | No        |
| Atributo | [Texto](text.md)             | Y   | No        |
| Value     | [Formato](formatted.md)   | No   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Conductor\_
</dt> <dd>

Nombre del token interno para un controlador. Clave principal de la tabla. Clave externa en la [tabla ODBCDriver](odbcdriver-table.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atributo
</dt> <dd>

Nombre del atributo de controlador. Clave principal de la tabla.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de cadena localizable para el atributo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las [acciones InstallODBC](installodbc-action.md) [y RemoveODBC](removeodbc-action.md) de las tablas [*de*](s-gly.md) secuencia procesan la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



