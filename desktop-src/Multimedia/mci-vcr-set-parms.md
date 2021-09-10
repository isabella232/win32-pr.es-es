---
title: MCI_VCR_SET_PARMS estructura (Vcr.h)
description: La estructura MCI VCR SET PARMS contiene parámetros para el \_ \_ comando \_ MCI SET para las \_ grabadoras de vídeo.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- MCI_VCR_SET_PARMS estructura Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369938"
---
# <a name="mci_vcr_set_parms-structure"></a>Estructura \_ PARMS de MCI VCR \_ SET \_

La **estructura MCI \_ VCR SET \_ \_ PARMS** contiene parámetros para el [**comando MCI \_ SET**](mci-set.md) para las grabadoras de vídeo.

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

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de hora actual.

</dd> <dt>

**dwAudio**
</dt> <dd>

No se usa.

</dd> <dt>

**dwTimeMode**
</dt> <dd>

Constante que especifica el origen de control de tiempo utilizado por el dispositivo. El origen de tiempo es un código de tiempo registrado en la cinta de vídeo o los contadores del dispositivo que detectan el movimiento de la cinta de vídeo.

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

Contenido de la pantalla.

</dd> <dt>

**dwTracking**
</dt> <dd>

Ajuste de velocidad utilizado al realizar el seguimiento de la velocidad de reproducción de VCR.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocidad de reproducción usada por el dispositivo como un entero. La velocidad de reproducción normal es 1000, la velocidad doble es 2000 y la media velocidad es 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Longitud de la cinta de vídeo cuando el dispositivo no puede detectar la longitud.

</dd> <dt>

**dwCounter**
</dt> <dd>

Nuevo valor de contador.

</dd> <dt>

**dwClock**
</dt> <dd>

Nueva hora del reloj.

</dd> <dt>

**dwPauseTimeout**
</dt> <dd>

Nuevo valor de tiempo de espera para el comando pause.

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

Longitud de la cinta de vídeo necesaria para estabilizar la salida de VCR.

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

Longitud de la cinta de vídeo necesaria para interrumpir el transporte de VCR cuando se emite un comando [**MCI \_ STOP**](mci-stop.md) o [**MCI \_ PAUSE.**](mci-pause.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**PAUSA \_ DE MCI**](mci-pause.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**MCI \_ STOP**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

