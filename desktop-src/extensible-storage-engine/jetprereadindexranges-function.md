---
description: 'Más información sobre: JetPrereadIndexRanges (Función)'
title: JetPrereadIndexRanges (Función)
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ff2d9e7c538e8aa8cc862fe9a72c0308e497fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986668"
---
# <a name="jetprereadindexranges-function"></a>JetPrereadIndexRanges (Función)


_**Se aplica a:** Windows | Windows Servidor_

La **función JetPrereadIndexRanges** prelega los índices para mejorar el rendimiento.

La **función JetPrereadIndexRanges** se introdujo en el Windows 8 operativo.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla con la que se emitirán los preleciones.

*rgIndexRanges*

Intervalos de claves que se van a leer previamente.

*cIndexRanges*

Número de intervalos de claves que se van a leer previamente, determinado por el número de elementos de *rgIndexRanges.*

*pcRangesPreread*

Número de intervalos de claves que se han leído previamente.

*rgcolumnidPreread*

Lista de id. de columna para las columnas de valor largo que se deben leer previamente. De forma predeterminada, solo se leerá previamente el registro en la página. Si las columnas de valores largos fuera de página deben leerse previamente, sus id. de columna deben pasarse a través de este parámetro.

*ccolumnidPreread*

Número de id. de columna para las columnas de valor largo que se deben leer previamente, determinado por el número de elementos de *rgcolumnidPreread.*

*grbit*

Grupo de bits que especifica cero o más de los valores de dirección de lectura previa enumerados en la tabla siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>Adelante</p> | <p>Leer previamente hacia delante.</p> | 
| <p>Atrás</p> | <p>Leer previamente hacia atrás.</p> | 
| <p>FirstPageOnly</p> | <p>Leer previamente solo la primera página de cualquier columna larga.</p> | 
| <p>NormalizedKey</p> | <p>Clave/marcador normalizado proporcionado en lugar del valor de columna.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores extensibles Storage Engine (ESE), vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 



#### <a name="remarks"></a>Observaciones

Si los registros con los intervalos de claves especificados no están en la caché del búfer, debe iniciar lecturas asincrónicas para llevar los registros a la caché del búfer de base de datos.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)
