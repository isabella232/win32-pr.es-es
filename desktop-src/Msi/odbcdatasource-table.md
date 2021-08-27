---
description: En la tabla ODBCDataSource se enumeran los orígenes de datos que pertenecen a la instalación.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Tabla ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43426ba7f2dd1214dc205213aa632558bbc44d81db5e6e32f7f7d66f82d30641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082725"
---
# <a name="odbcdatasource-table"></a>Tabla ODBCDataSource

En la tabla ODBCDataSource se enumeran los orígenes de datos que pertenecen a la instalación.

La tabla ODBCDataSource tiene las columnas siguientes.



| Columna            | Tipo                         | Clave | Nullable |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Identificador](identifier.md) | Y   | N        |
| Componente\_       | [Identificador](identifier.md) | N   | N        |
| Descripción       | [Texto](text.md)             | N   | N        |
| DriverDescription | [Texto](text.md)             | N   | N        |
| Registro      | [Entero](integer.md)       | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>Datasource
</dt> <dd>

Nombre del token interno para el origen de datos. Clave principal de la tabla.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la [tabla Component](component-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción registrada para este origen de datos. Este valor no se puede localizar. Las descripciones del origen de datos ODBC no pueden SQL \_ MAX \_ DSN \_ LENGTH.

</dd> <dt>

<span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription
</dt> <dd>

Controlador asociado que puede ser existente previamente. Este valor no se puede localizar.

</dd> <dt>

<span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registro
</dt> <dd>

Este campo especifica el tipo de registro para el origen de datos.



| Constante                                      | Hexadecimal | Decimal | Descripción                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| **msidbODBCDataSourceRegistrationPerMachine** | 0x000       | 0       | El origen de datos se registra por máquina. |
| **msidbODBCDataSourceRegistrationPerUser**    | 0x001       | 1       | El origen de datos se registra por usuario.    |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las [acciones InstallODBC](installodbc-action.md) [y RemoveODBC](removeodbc-action.md) de las tablas [*de*](s-gly.md) secuencia procesan la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



