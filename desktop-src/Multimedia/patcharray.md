---
title: PATCHARRAY (mmsystem. h)
description: PATCHARRAY es un tipo que se usa para definir una matriz de revisiones MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905656"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY es un tipo que se usa para definir una matriz de revisiones MIDI.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Cada elemento de la matriz corresponde a una revisión con cada uno de los 16 bits que representa uno de los 16 canales MIDI. Los bits se establecen para cada uno de los canales que usan esa revisión concreta. Por ejemplo, si el número de revisión 0 se usa en los canales MIDI físicos 0 y 8, el elemento 0 de la matriz se debe establecer en 0x0101.

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

 

 





