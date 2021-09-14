---
title: KEYARRAY (Mmsystem.h)
description: KEYARRAY especifica un tipo utilizado para definir una matriz de claves.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- KEYARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246171"
---
# <a name="keyarray"></a>KEYARRAY

KEYARRAY especifica un tipo utilizado para definir una matriz de claves.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**KEYARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Cada elemento de la matriz corresponde a una revisión de revisiones basada en claves con cada uno de los 16 bits que representan uno de los 16 canales DE LÍNEA. Los bits se establecen para cada uno de los canales que usan esa revisión concreta. Por ejemplo, si los canales físicos 9 y 15 usan la revisión de revisiones para el número de clave 60, el elemento 60 de la matriz debe establecerse en 0x8200.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Versión<br/>                  | Interfaz digital de instrumentar música (MIDI), tipos DE MIDI<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos DE MIDI](midi-event-types.md)
</dt> </dl>

 

 





