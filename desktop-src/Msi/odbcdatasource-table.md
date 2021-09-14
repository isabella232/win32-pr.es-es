---
description: En la tabla ODBCDataSource se enumeran los orígenes de datos que pertenecen a la instalación.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Tabla ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251072"
---
# <a name="odbcdatasource-table"></a>Tabla ODBCDataSource

En la tabla ODBCDataSource se enumeran los orígenes de datos que pertenecen a la instalación.

La tabla ODBCDataSource tiene las columnas siguientes.



| Columna            | Tipo                         | Clave | Nullable |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Identificador](identifier.md) | Y   | No        |
| Componente\_       | [Identificador](identifier.md) | No   | No        |
| Descripción       | [Texto](text.md)             | No   | No        |
| DriverDescription | [Texto](text.md)             | No   | No        |
| Registro      | [Entero](integer.md)       | No   | No        |



 

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

## <a name="remarks"></a>Observaciones

Las [acciones InstallODBC](installodbc-action.md) [y RemoveODBC](removeodbc-action.md) de las tablas [*de*](s-gly.md) secuencia procesan la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



