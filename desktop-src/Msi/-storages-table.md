---
description: En \_ la tabla Storages se enumeran los almacenamientos de datos OLE incrustados. Se trata de una tabla temporal, creada solo cuando una instrucción SQL referencia.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159300"
---
# <a name="_storages-table"></a>\_Tabla de almacenamientos

En \_ la tabla Storages se enumeran los almacenamientos de datos OLE incrustados. Se trata de una tabla temporal, creada solo cuando una instrucción SQL referencia.



| Columna | Tipo                 | Clave | Nullable |
|--------|----------------------|-----|----------|
| Nombre   | [Texto](text.md)     | Y   | N        |
| Datos   | [Binario](binary.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Clave única que identifica el almacenamiento. La longitud máxima de Name es de 31 caracteres.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Datos
</dt> <dd>

Datos binarios sin formato.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para agregar un almacenamiento OLE a una base de datos, cree un nuevo registro en la tabla Storages y escriba el nombre del almacenamiento \_ en la columna Nombre. Use [**MsiRecordSetStream para**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) copiar datos en la columna Datos de este registro. Por último, use [**MsiViewModify para**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) insertar el registro en la \_ tabla Storages.

Los datos no se pueden leer de \_ la tabla Storages. Sin embargo, se puede consultar la tabla Storages \_ para comprobar la existencia de un almacenamiento específico. Esto significa que no es posible mover un almacenamiento OLE de una base de datos a otra. En su lugar, debe importar el archivo de almacenamiento original en la nueva base de datos. Para eliminar un almacenamiento OLE, captura el registro que contiene los datos binarios, establece la columna Datos de la tabla \_ Storages en NULL y, a continuación, actualiza el registro. Un método alternativo consiste simplemente en eliminar el registro mediante [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una consulta SQL sin formato.

Para cambiar el nombre de un almacenamiento OLE, actualice la columna Nombre del registro.

Si se coloca una retención en esta tabla mediante SQL (ALTER TABLE) <table> HOLD) o se agrega una columna con HOLD, la tabla debe liberarse mediante FREE. Los almacenamientos no se escriben hasta que la tabla se ha liberado o confirmado.

 

 



