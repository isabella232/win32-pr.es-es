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
ms.openlocfilehash: 546ace6b93328c3420a33c131250510d8421491b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470841"
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

### <a name="remarks"></a>Comentarios

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


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
