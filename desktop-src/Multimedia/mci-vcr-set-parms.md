---
title: MCI_VCR_SET_PARMS estructura (VCR. h)
description: La estructura de parms de VCR de MCI \_ \_ \_ contiene parámetros para el \_ comando MCI set para los grabadores de casete de vídeo.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- Estructura de MCI_VCR_SET_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422553"
---
# <a name="mci_vcr_set_parms-structure"></a>\_Estructura parms del vídeo de MCI \_ set \_

La estructura de **\_ \_ \_ parms de VCR de MCI** contiene parámetros para el comando [**MCI \_ set**](mci-set.md) para los grabadores de casete de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de hora actual.

</dd> <dt>

**dwAudio**
</dt> <dd>

No se utiliza.

</dd> <dt>

**dwTimeMode**
</dt> <dd>

Constante que especifica el origen de tiempo utilizado por el dispositivo. El origen de tiempo es un código de tiempo que se graba en una cinta de vídeo o los contadores del dispositivo que tienen en cuenta el movimiento de la cinta de vídeo.

</dd> <dt>

**dwRecordFormat**
</dt> <dd>

Velocidad de grabación.

</dd> <dt>

**dwCounterFormat**
</dt> <dd>

Formato de un nuevo valor de tiempo de contador.

</dd> <dt>

**dwIndex**
</dt> <dd>

Contenido de la presentación en pantalla.

</dd> <dt>

**dwTracking**
</dt> <dd>

Ajuste de velocidad usado cuando se realiza el seguimiento de la velocidad de reproducción de VCR.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocidad de reproducción utilizada por el dispositivo como un entero. La velocidad de reproducción normal es 1000, la velocidad doble es 2000 y la velocidad media es 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Longitud de la cinta de vídeo cuando el dispositivo no detecta la longitud.

</dd> <dt>

**dwCounter**
</dt> <dd>

Nuevo valor del contador.

</dd> <dt>

**dwClock**
</dt> <dd>

Nueva hora de reloj.

</dd> <dt>

**dwPauseTimeout**
</dt> <dd>

Nuevo valor de tiempo de espera para el comando pausar.

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

Duración de la cinta de vídeo necesaria para estabilizar la salida del VCR.

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

Longitud de la cinta de vídeo necesaria para frenar el transporte de VCR cuando se emite un comando [**MCI \_ Stop**](mci-stop.md) o [**MCI \_ PAUSE**](mci-pause.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**pausa de MCI \_**](mci-pause.md)
</dt> <dt>

[**MCI \_ set**](mci-set.md)
</dt> <dt>

[**detención de MCI \_**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

