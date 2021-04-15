---
title: KEYARRAY (mmsystem. h)
description: KEYARRAY especifica un tipo que se usa para definir una matriz de claves.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- KEYARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676765"
---
# <a name="keyarray"></a>KEYARRAY

KEYARRAY especifica un tipo que se usa para definir una matriz de claves.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**KEYARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Cada elemento de la matriz corresponde a una revisión de percusión basada en claves con cada uno de los 16 bits que representa uno de los 16 canales MIDI. Los bits se establecen para cada uno de los canales que usan esa revisión concreta. Por ejemplo, si la revisión de percusión para el número de clave 60 se usa en los canales MIDI físicos 9 y 15, el elemento 60 de la matriz se debe establecer en 0x8200.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Versión<br/>                  | Interfaz digital de instrumentos musicales (MIDI), tipos MIDI<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos MIDI](midi-event-types.md)
</dt> </dl>

 

 





