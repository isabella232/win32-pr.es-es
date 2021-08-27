---
description: 'Más información sobre: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 82a0df37215122e943955f32aeed4d39dd70b268
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983158"
---
# <a name="jet_ls"></a>JET_LS


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_ls"></a>JET_LS

El **JET_LS** tipo de datos contiene un identificador de contexto para el almacenamiento local (LS). Este identificador puede estar asociado a un cursor o una tabla y puede hacer referencia a recursos asignados dinámicamente.

**Windows XP: JET_LS** se introduce en Windows XP.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Tipo de datos

JET_LS

Un valor de JET_LSNil indica un identificador de contexto no válido.

### <a name="remarks"></a>Observaciones

Un identificador de contexto se asocia inicialmente al **tipo JET_LS** datos, mediante [JetSetLS.](./jetsetls-function.md) El identificador de contexto se puede recuperar del tipo **JET_LS** datos, mediante [JetGetLS.](./jetgetls-function.md)

El identificador de contexto se puede desasociar explícitamente del tipo **de JET_LS** datos mediante [JetGetLS](./jetgetls-function.md) con JET_bitLSReset. Como alternativa, el identificador de contexto se puede desasociar implícitamente del tipo de datos **JET_LS** cuando el motor de base de datos libera el objeto subyacente como resultado de una acción directa o indirecta por parte de la aplicación. En el caso implícito, se emite una devolución de llamada en tiempo de ejecución a la aplicación para que pueda limpiar el identificador de contexto. Para obtener más información sobre la desasociación implícita del **tipo JET_LS** datos, vea [JetSetLS](./jetsetls-function.md).

Las marcas siguientes están asociadas al tipo JET_LS datos.


| <p>Término</p> | <p>Descripción</p> | 
|-------------|--------------------|
| <p>JET_bitLSReset</p> | <p>El identificador de contexto se desasocia del objeto .</p> | 
| <p>JET_bitLSCursor</p> | <p>Establezca o recupere el almacenamiento local asociado a un cursor de tabla.</p> | 
| <p>JET_bitLSTable</p> | <p>Establezca o recupere el almacenamiento local asociado a una tabla.</p> | 
| <p>JET_LSNil</p> | <p>El identificador de contexto no es válido.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
