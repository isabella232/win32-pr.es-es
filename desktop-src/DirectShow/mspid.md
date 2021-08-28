---
description: 'Nota: Esta API está en desuso. Las nuevas aplicaciones no deben usarla. El tipo de datos MSPID identifica el propósito de un flujo multimedia.'
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (Mmstream.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9d274fc4131c0aa4494d610cbe1145ad79b848b5f6280d4ad6a10b298a8b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075755"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> Esta API está en desuso. Las nuevas aplicaciones no deben usarla.

 

El **tipo de datos MSPID** identifica el propósito de un flujo multimedia.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Comentarios

**MSPID** es simplemente una definición de tipo para GUID. Se definen los siguientes MSPID.



| Value               | Descripción           |
|---------------------|-----------------------|
| MSPID \_ PrimaryVideo | Secuencia de vídeo principal. |
| MSPID \_ PrimaryAudio | Secuencia de audio principal. |



 

El **tipo REFMSPID** define una referencia a **un MSPID**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mmstream.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos de streaming multimedia](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




