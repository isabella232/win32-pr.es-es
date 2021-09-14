---
title: PATCHARRAY (Mmsystem.h)
description: PATCHARRAY es un tipo que se usa para definir una matriz de revisiones DE MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161397"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY es un tipo que se usa para definir una matriz de revisiones DE MIDI.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Cada elemento de la matriz corresponde a una revisión con cada uno de los 16 bits que representan uno de los 16 canales DE MIDI. Los bits se establecen para cada uno de los canales que usan esa revisión concreta. Por ejemplo, si los canales FÍSICOs 0 y 8 usan el número de revisión 0, el elemento 0 de la matriz debe establecerse en 0x0101.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Versión<br/>                  | Interfaz digital instrumentable (MIDI), tipos DE MIDI<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tipos DE MIDI](midi-event-types.md)
</dt> </dl>

 

 





