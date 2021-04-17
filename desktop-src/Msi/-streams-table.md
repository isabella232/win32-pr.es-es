---
description: En la \_ tabla streams se enumeran los flujos de datos OLE incrustados. Se trata de una tabla temporal que solo se crea cuando se hace referencia a ella mediante una instrucción SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667081"
---
# <a name="_streams-table"></a>\_Tabla de secuencias

En la \_ tabla streams se enumeran los flujos de datos OLE incrustados. Se trata de una tabla temporal que solo se crea cuando se hace referencia a ella mediante una instrucción SQL.



| Columna | Tipo                 | Clave | Nullable |
|--------|----------------------|-----|----------|
| Nombre   | [Texto](text.md)     | Y   | N        |
| Datos   | [Binario](binary.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Una clave única que identifica la secuencia. La longitud máxima del nombre es de 62 caracteres.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Data
</dt> <dd>

Datos binarios sin formato.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para copiar un flujo de datos OLE (por ejemplo, un objeto del tipo de datos [binario](binary.md) ) de un archivo en una base de datos, cree un registro en la \_ tabla streams y escriba el nombre del flujo de datos en la columna Nombre de este registro y copie los datos del archivo en la columna de datos mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama). Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el nuevo registro en la tabla.

Para leer un flujo de datos binarios incrustado en una base de datos, utilice una consulta SQL para buscar y recuperar el registro que contiene los datos binarios. Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) para leer los datos binarios en un búfer.

Para trasladar un flujo de datos binarios de una base de datos a otra, exporte primero los datos a un archivo. Use una consulta SQL para buscar el flujo de datos en el archivo y use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar los datos del archivo en la columna de datos de \_ la tabla de secuencias de la segunda base de datos. Esto garantiza que cada base de datos tiene su propia copia de los datos binarios. No se pueden trasladar datos binarios de una base de datos a otra simplemente mediante la captura de un registro con los datos de la primera base de datos y su inserción en la segunda base de datos.

Para eliminar un flujo de datos, recupere el registro y establezca la columna de datos en NULL antes de actualizar el registro. Otro método consiste en quitar el registro de la tabla y eliminarlo mediante [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una consulta SQL sin formato. No se debe capturar un flujo en un registro si se elimina la secuencia de la tabla.

Para cambiar el nombre de un flujo de datos OLE, actualice la columna ' name ' del registro.

Si se coloca una retención en esta tabla mediante SQL (ALTER TABLE <table> HOLD) o se agrega una columna con Reverse, la tabla se debe liberar mediante FREE. Las secuencias no se escriben hasta que la tabla se ha liberado o confirmado.

 

 



