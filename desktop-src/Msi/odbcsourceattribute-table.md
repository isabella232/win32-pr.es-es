---
description: La tabla ODBCSourceAttribute contiene información sobre los atributos de los orígenes de datos.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Tabla ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d84ca19dfd059df4ff8f79d9409ef23288800f09e84d45e1b55d81bc8641e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082715"
---
# <a name="odbcsourceattribute-table"></a>Tabla ODBCSourceAttribute

La tabla ODBCSourceAttribute contiene información sobre los atributos de los orígenes de datos.

La tabla ODBCSourceAttribute tiene las columnas siguientes.



| Columna       | Tipo                         | Clave | Nullable |
|--------------|------------------------------|-----|----------|
| Datasource\_ | [Identificador](identifier.md) | Y   | N        |
| Atributo    | [Texto](text.md)             | Y   | N        |
| Value        | [Formato](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>Datasource\_
</dt> <dd>

Nombre del token interno para el origen de datos. Clave principal de la tabla.

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atributo
</dt> <dd>

Nombre del atributo de origen de datos. Clave principal de la tabla.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de cadena localizable para el atributo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las [acciones InstallODBC](installodbc-action.md) [y RemoveODBC](removeodbc-action.md) de las tablas [*de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



