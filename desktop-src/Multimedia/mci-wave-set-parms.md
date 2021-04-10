---
title: MCI_WAVE_SET_PARMS estructura (Mciapi. h)
description: La \_ estructura parms de MCI Wave \_ set \_ contiene información para el \_ comando MCI set para dispositivos de audio de forma de onda.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- Estructura de MCI_WAVE_SET_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905571"
---
# <a name="mci_wave_set_parms-structure"></a>\_Estructura parms de MCI Wave \_ set \_

La estructura **parms de MCI \_ Wave \_ set \_** contiene información para el comando [**MCI \_ set**](mci-set.md) para dispositivos de audio de forma de onda.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de hora del dispositivo.

</dd> <dt>

**dwAudio**
</dt> <dd>

Número de canal para la salida de audio. Se usa normalmente al activar o desactivar un canal.

</dd> <dt>

**wInput**
</dt> <dd>

Canal de entrada de audio.

</dd> <dt>

**wOutput**
</dt> <dd>

Dispositivo de salida que se va a usar. Por ejemplo, este valor podría ser 2 Si un sistema tuviera dos tarjetas de sonido instaladas.

</dd> <dt>

**wFormatTag**
</dt> <dd>

Formato de los datos de audio de forma de onda, como PCM con formato de onda \_ \_ . Los valores posibles se definen en Mmreg. h.

</dd> <dt>

**wReserved2**
</dt> <dd>

Reservado.

</dd> <dt>

**nChannels**
</dt> <dd>

Mono (1) o estéreo (2).

</dd> <dt>

**wReserved3**
</dt> <dd>

Reservado.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Muestras por segundo.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Velocidad de muestra en bytes por segundo.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Alineación de bloque de los datos.

</dd> <dt>

**wReserved4**
</dt> <dd>

Reservado.

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits por muestra.

</dd> <dt>

**wReserved5**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ set**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

