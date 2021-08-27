---
description: 'Más información sobre: función JET_PFNREALLOC de devolución de llamada'
title: JET_PFNREALLOC Callback (Función)
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7427a28752384f6c30e050458e5844dcaedd1a7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989148"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC Callback (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC Callback (Función)

La JET_PFNREALLOC es una devolución de llamada compatible con [la](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación utilizada por [JetEnumerateColumns](./jetenumeratecolumns-function.md) para asignar memoria para sus búferes de salida.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parámetros

*pvContext*

Puntero de contexto dado [a JetEnumerateColumns.](./jetenumeratecolumns-function.md) Este puntero de contexto se puede usar para transmitir el estado del autor de la llamada [de JetEnumerateColumns](./jetenumeratecolumns-function.md) a la implementación de esta devolución de llamada.

*Pv*

Si no es NULL, especifica un puntero a un bloque de memoria asignado previamente por esta devolución de llamada. Si es NULL, se asignará un nuevo bloque de memoria del tamaño solicitado.

*Cb*

Nuevo tamaño del bloque de memoria en bytes. Si este parámetro es 0 (cero) y se especifica un bloque de memoria, se liberará ese bloque de memoria.

### <a name="return-value"></a>Valor devuelto

El sistema puede generar códigos correctos o de error como resultado de una llamada a esta función. Para obtener información sobre cómo devolver estos códigos como HULT, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>Correcto</p> | <p>Si se especificó un bloque de memoria asignado previamente y se especificó un nuevo tamaño de cero, ese bloque se libera y se devuelve NULL. Si se especificó un bloque de memoria asignado previamente y se especificó un nuevo tamaño distinto de cero, se devuelve el bloque de memoria reasignado. Si no se especificó ningún bloque de memoria, se devuelve un bloque de memoria recién asignado del tamaño especificado.</p> | 
| <p>Error</p> | <p>Se devolverá NULL. Si se proporcionó un bloque de memoria asignado previamente, ese bloque permanecerá asignado.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
