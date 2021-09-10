---
title: MCI_WAVE_SET_PARMS estructura (Mciapi.h)
description: La estructura MCI \_ WAVE \_ SET \_ PARMS contiene información para el comando MCI \_ SET para dispositivos de audio de onda.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- MCI_WAVE_SET_PARMS estructura Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369955"
---
# <a name="mci_wave_set_parms-structure"></a>Estructura MCI \_ WAVE \_ SET \_ PARMS

La **estructura MCI \_ WAVE SET \_ \_ PARMS** contiene información para el [**comando MCI \_ SET**](mci-set.md) para dispositivos de audio de onda.

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

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de hora del dispositivo.

</dd> <dt>

**dwAudio**
</dt> <dd>

Número de canal para la salida de audio. Normalmente se usa al activar o desactivar un canal.

</dd> <dt>

**wInput**
</dt> <dd>

Canal de entrada de audio.

</dd> <dt>

**wOutput**
</dt> <dd>

Dispositivo de salida que se usará. Por ejemplo, este valor podría ser 2 si un sistema tuviera dos tarjetas de sonido instaladas.

</dd> <dt>

**wFormatTag**
</dt> <dd>

Formato de los datos de audio de forma de onda, como WAVE \_ FORMAT \_ PCM. Los valores posibles se definen en Mmreg.h.

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

Ejemplos por segundo.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Frecuencia de muestreo en bytes por segundo.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Bloquear la alineación de los datos.

</dd> <dt>

**wReserved4**
</dt> <dd>

Reservado.

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits por ejemplo.

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
| Encabezado<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

