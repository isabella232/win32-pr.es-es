---
description: La \_ Secuencias enumera los flujos de datos OLE incrustados. Se trata de una tabla temporal, creada solo cuando una instrucción SQL referencia.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f3796a3abb402027dc9985991a6ba673f5381d8f35657e7d80b0714c40f1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013343"
---
# <a name="_streams-table"></a>\_Secuencias Mesa

La \_ Secuencias enumera los flujos de datos OLE incrustados. Se trata de una tabla temporal, creada solo cuando una instrucción SQL referencia.



| Columna | Tipo                 | Clave | Nullable |
|--------|----------------------|-----|----------|
| Nombre   | [Texto](text.md)     | Y   | N        |
| Datos   | [Binario](binary.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Clave única que identifica la secuencia. La longitud máxima de Name es de 62 caracteres.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Datos
</dt> <dd>

Datos binarios sin formato.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para copiar un flujo de datos OLE (por ejemplo, un objeto del tipo de datos [Binary)](binary.md) de un archivo en una base de datos, cree un registro en la tabla Secuencias y escriba el nombre del flujo de datos en la columna Nombre de este registro y copie los datos del archivo en la columna Datos mediante \_ [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama). Use [**MsiViewModify para**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) insertar el nuevo registro en la tabla.

Para leer un flujo de datos binario insertado en una base de datos, use una consulta SQL para buscar y capturar el registro que contiene los datos binarios. Use [**MsiRecordReadStream para**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) leer los datos binarios en un búfer.

Para mover un flujo de datos binarios de una base de datos a otra, exporte primero los datos a un archivo. Use una consulta SQL para buscar el flujo de datos en el archivo y use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar los datos del archivo en la columna Datos de Secuencias tabla de la segunda base de \_ datos. Esto garantiza que cada base de datos tenga su propia copia de los datos binarios. No se pueden mover datos binarios de una base de datos a otra simplemente capturando un registro con los datos de la primera base de datos e insertándose en la segunda base de datos.

Para eliminar un flujo de datos, captura el registro y establece la columna Datos en NULL antes de actualizar el registro. Otro método consiste en quitar el registro de la tabla y eliminarlo mediante [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una consulta SQL sin formato. No se debe capturar una secuencia en un registro si la secuencia se elimina de la tabla.

Para cambiar el nombre de un flujo de datos OLE, actualice la columna "Name" del registro.

Si se coloca una retención en esta tabla mediante SQL (ALTER TABLE) <table> HOLD) o se agrega una columna con HOLD, la tabla debe liberarse mediante FREE. Secuencias se escriben hasta que la tabla se ha liberado o confirmado.

 

 



