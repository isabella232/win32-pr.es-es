---
title: KEYARRAY (Mmsystem.h)
description: KEYARRAY especifica un tipo utilizado para definir una matriz de claves.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- KEYARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c5f578b912a7b184f9f455bc4a730132b2316472d061532c48847c312302d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140045"
---
# <a name="keyarray"></a>KEYARRAY

KEYARRAY especifica un tipo utilizado para definir una matriz de claves.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**KEYARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Cada elemento de la matriz corresponde a una revisión de revisión de revisión basada en claves con cada uno de los 16 bits que representan uno de los 16 canales DE LÍNEA. Los bits se establecen para cada uno de los canales que usan esa revisión concreta. Por ejemplo, si los canales FÍSICOs 9 y 15 usan la revisión de la clave 60, el elemento 60 de la matriz debe establecerse en 0x8200.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Versión<br/>                  | Interfaz digital instrumentable (MIDI), tipos DE MIDI<br/>                                        |
| Header<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos DE MIDI](midi-event-types.md)
</dt> </dl>

 

 





