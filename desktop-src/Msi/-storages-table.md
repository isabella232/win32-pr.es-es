---
description: La \_ tabla Storages enumera los almacenamientos de datos OLE incrustados. Se trata de una tabla temporal que solo se crea cuando se hace referencia a ella mediante una instrucción SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909166"
---
# <a name="_storages-table"></a>\_Tabla Storages

La \_ tabla Storages enumera los almacenamientos de datos OLE incrustados. Se trata de una tabla temporal que solo se crea cuando se hace referencia a ella mediante una instrucción SQL.



| Columna | Tipo                 | Clave | Nullable |
|--------|----------------------|-----|----------|
| Nombre   | [Texto](text.md)     | Y   | N        |
| Datos   | [Binario](binary.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Una clave única que identifica el almacenamiento. La longitud máxima del nombre es de 31 caracteres.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Data
</dt> <dd>

Datos binarios sin formato.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para agregar un almacenamiento OLE a una base de datos, cree un nuevo registro en la \_ tabla Storages y escriba el nombre del almacenamiento en la columna nombre. Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar datos en la columna de datos de este registro. Por último, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la \_ tabla de almacenamiento.

No se pueden leer los datos de la \_ tabla de almacenamiento. Sin embargo, \_ se puede consultar la tabla de almacenamiento para comprobar la existencia de un almacenamiento específico. Esto significa que no es posible trasladar un almacenamiento OLE de una base de datos a otra. En su lugar, debe importar el archivo de almacenamiento original en la nueva base de datos. Para eliminar un almacenamiento OLE, recupere el registro que contiene los datos binarios, establezca la columna de datos de la \_ tabla Storages en NULL y, a continuación, actualice el registro. Un método alternativo consiste en eliminar simplemente el registro mediante [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una consulta SQL sin formato.

Para cambiar el nombre de un almacenamiento OLE, actualice la columna Nombre del registro.

Si se coloca una retención en esta tabla mediante SQL (ALTER TABLE <table> HOLD) o se agrega una columna con Reverse, la tabla se debe liberar mediante FREE. Los almacenamientos no se escriben hasta que la tabla se ha liberado o confirmado.

 

 



