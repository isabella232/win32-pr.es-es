---
description: 'Más información sobre: Parámetros informativos'
title: Parámetros informativos
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: cd932f64956e1a00aae5925b97dbf6c35ecc2661
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987608"
---
# <a name="informational-parameters"></a>Parámetros informativos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="informational-parameters"></a>Parámetros informativos

Este tema contiene parámetros que se usan para exponer información sobre el motor de base de datos.

*JET_paramKeyMost*  
134  

Este parámetro de solo lectura indica la longitud máxima de clave de índice permitido que se puede seleccionar para el tamaño de página de la base de datos actual (según lo configurado por JET_paramDatabasePageSize).


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>JET_cbKeyMost4KBytePage</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>255 – 65535</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>N/D</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>N/D</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>A partir de Windows Server 2008 y Windows Vista</p> | 



*JET_paramMaxColtyp*  
131  

Este parámetro de solo lectura devuelve el número [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) para esa versión del motor de base de datos. Este valor se puede usar para comprobar la compatibilidad de una aplicación [JET_COLTYP](./jet-coltyp.md). Si un valor [JET_COLTYP](./jet-coltyp.md) es menor que el valor de este parámetro, el motor de base de datos lo admite.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>JET_coltypUnsignedShort + 1</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0 – 255</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>N/D</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>N/D</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>A partir de Windows Server 2008 y Windows Vista</p> | 



*JET_paramLVChunkSizeMost*  
163  

Parámetro de solo lectura que devuelve el tamaño del fragmento de valor largo en función del tamaño de página configurado. Si se va a leer o escribir un valor largo con varias llamadas a Jet{Set,Retrieve}Column, el uso de un búfer cuyo tamaño es un múltiplo del tamaño del fragmento es más eficaz.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>Página de 2 kb = 1966 bytes<br />Página de 4 kb = 4014 bytes<br />Página de 8 kb = 8110 bytes<br />Página de 16 kb = 4050 bytes<br />Página de 32 kb = 8150 bytes</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0-10000</p> | 
| <p>Ámbito:</p> | <p></p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p></p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p></p> | 
| <p>Afecta al diseño físico:</p> | <p></p> | 
| <p>Afecta a la confiabilidad:</p> | <p></p> | 
| <p>Afecta al rendimiento:</p> | <p></p> | 
| <p>Afecta a los recursos:</p> | <p></p> | 
| <p>Disponibilidad:</p> | <p></p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
