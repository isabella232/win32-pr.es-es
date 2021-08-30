---
title: MM_MIM_CLOSE mensaje (Mmsystem.h)
description: El mensaje MM \_ MIM CLOSE se envía a una ventana cuando se cierra un dispositivo de entrada DE \_ LÍNEA.
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- MM_MIM_CLOSE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1ee579f09fbd379f1fa353d602657194b0848d040210a713d0492a7e42311
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807395"
---
# <a name="mm_mim_close-message"></a>Mensaje MM \_ MIM \_ CLOSE

El **mensaje MM MIM \_ \_ CLOSE** se envía a una ventana cuando se cierra un dispositivo de entrada DE LÍNEA.


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Identificador del dispositivo de entrada DE LÍNEA que se ha cerrado.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Reservado; no use.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaz digital de instrumentos digitales (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensajes DE MIDI](midi-messages.md)
</dt> </dl>

 

 





