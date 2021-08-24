---
title: PATCHARRAY (Mmsystem.h)
description: PATCHARRAY es un tipo que se usa para definir una matriz de revisiones DE MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1d14696d7bb76827f902609cb1411f7890adeac53092e1b66b7eda16604320
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806075"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY es un tipo que se usa para definir una matriz de revisiones DE MIDI.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Cada elemento de la matriz corresponde a una revisión con cada uno de los 16 bits que representan uno de los 16 canales DE LÍNEA. Los bits se establecen para cada uno de los canales que usan esa revisión concreta. Por ejemplo, si los canales físicos 0 y 8 usan el número de revisión 0, el elemento 0 de la matriz debe establecerse en 0x0101.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Versión<br/>                  | Interfaz digital de instrumentar música (MIDI), tipos DE MIDI<br/>                                        |
| Header<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos DE MIDI](midi-event-types.md)
</dt> </dl>

 

 





