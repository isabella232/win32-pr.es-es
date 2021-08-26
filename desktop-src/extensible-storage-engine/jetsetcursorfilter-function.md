---
description: 'Más información sobre: JetSetCursorFilter (Función)'
title: JetSetCursorFilter (Función)
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5958d288e8b101795d1c8e4b4db789ade4b98418
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477521"
---
# <a name="jetsetcursorfilter-function"></a>JetSetCursorFilter (Función)


_**Se aplica a:** Windows | Windows Servidor_

La **función JetSetCursorFilter** establece una matriz de filtros simples para la [función JetMove.](./jetmove-function.md)

La **función JetSetCursorFilter** se introdujo en el Windows 8 operativo.

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Cursor que se colocará.

*rgFilters*

Filtros de registros simples.

*cFilters*

Número de filtros.

*grbit*

Grupo de bits que especifica cero o más de las opciones de movimiento enumeradas en la tabla siguiente.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>Ninguno</p> | <p>Opciones predeterminadas</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores extensibles Storage Engine (ESE), vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 



#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JetMove](./jetmove-function.md)  
[JET_ERR](./jet-err.md)
