---
description: 'Más información sobre: Parámetros de devolución de llamada'
title: Parámetros de devolución de llamada
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: a7b904c090852ea3990ac78e37a7ca851e152968
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465222"
---
# <a name="callback-parameters"></a>Parámetros de devolución de llamada


_**Se aplica a:** Windows | Windows Servidor_

## <a name="callback-parameters"></a>Parámetros de devolución de llamada

Este tema contiene parámetros que se usan para las devoluciones de llamada.

*JET_paramDisableCallbacks*  
65  

Este parámetro deshabilita todas las devoluciones de llamada del motor de base de datos a las funciones proporcionadas por la aplicación. Está pensado principalmente para admitir las utilidades del motor de base de datos y no está pensado para usarse en la aplicación.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramEnablePersistedCallbacks*  
156  

Este parámetro permite el uso de devoluciones de llamada persistentes en la base de datos. En las versiones anteriores a Windows Vista, el uso de devoluciones de llamada persistentes estaba habilitado de forma predeterminada. Las aplicaciones ahora deben habilitar explícitamente el uso de devoluciones de llamada persistentes en tiempo de ejecución mediante este parámetro. Si no se establece este parámetro, cualquier operación de base de datos que requiera la invocación de una devolución de llamada producirá un error JET_errCallbackFailed. Este parámetro no afecta a las devoluciones de llamada especificadas en tiempo de ejecución con los siguientes mecanismos: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)o un parámetro de devolución de llamada explícito a una API jet. Todavía es posible crear elementos de esquema que contengan devoluciones de llamada persistentes incluso cuando no se permite el uso de esas devoluciones de llamada persistentes. Cuando este parámetro se establece en false, invalida JET_paramDisableCallbacks.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramRuntimeCallback*  
73  

Este parámetro configura el motor con una función de devolución de llamada en tiempo de ejecución que implementa [la JET_CALLBACK](./jet-callback-callback-function.md) ejecución. Se puede llamar a esta devolución de llamada por los siguientes motivos: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)o [JET_cbtypNull](./jet-cbtyp.md). Consulte [JetSetLS para](./jetsetls-function.md) obtener más información.


| | | <p>Valor predeterminado:</p> | <p>NULL</p> | | <p>Escriba:</p> | <p>Puntero de función (JET_API_PTR)</p> | | <p>Intervalo válido:</p> | <p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
