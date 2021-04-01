---
title: Comando MCI_RECORD (mmsystem. h)
description: El \_ comando MCI record inicia la grabación desde la posición actual o desde una ubicación especificada hasta otra ubicación especificada.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- Comando de MCI_RECORD de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150396"
---
# <a name="mci_record-command"></a>\_Comando MCI record

El comando [**MCI \_ Record**](mci-record-parms.md) inicia la grabación desde la posición actual o desde una ubicación especificada hasta otra ubicación especificada. Los dispositivos VCR y de onda-audio reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms del registro MCI**](mci-record-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando es compatible con los dispositivos que devuelven **true** cuando se llama al comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con el \_ marcador MCI GETDEVCAPS \_ Can \_ Record. En el caso del controlador MCIWAVE, todos los datos registrados después de abrir un archivo se descartan si el archivo se cierra sin guardarlo.

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten el registro de MCI \_ :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde
</dt> <dd>

Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpRecord*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) . Si \_ no se especifica MCI desde, la ubicación inicial toma como valor predeterminado la posición actual.

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_inserción de registros MCI \_
</dt> <dd>

La información que se acaba de grabar se debe insertar o pegar en los datos existentes. Es posible que algunos dispositivos no lo admitan. Si se admite, este es el valor predeterminado.

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>\_sobrescritura del registro de MCI \_
</dt> <dd>

Los datos deben sobrescribir los datos existentes. MCIWAVE. El dispositivo DRV devuelve \_ la función no admitida MCIERR \_ en respuesta a esta marca.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpRecord*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) . Si \_ no se especifica MCI en, la ubicación final toma como valor predeterminado el final del contenido.

</dd> </dl>

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>\_secuencia de \_ audio de registro DGV \_ de MCI \_
</dt> <dd>

Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpRecord*. Si omite esta marca, los datos de audio se registran en la primera secuencia física.

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>retención de registro de MCI \_ DGV \_ \_
</dt> <dd>

Cuando se detiene la grabación, la pantalla contendrá la última imagen y no se reanudará mostrando el vídeo hasta que se emita un comando del [ \_ monitor MCI](mci-monitor.md) .

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_secuencia de \_ vídeo de registro \_ \_ de MCI DGV
</dt> <dd>

Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpRecord*. Si omite esta marca, los datos de vídeo se registran en la primera secuencia física.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect
</dt> <dd>

Se especifica un rectángulo en el miembro **RC** de la estructura identificada por *lpRecord*. El rectángulo especifica la región de la entrada externa usada como origen para los píxeles comprimidos y guardados. Este rectángulo tiene como valor predeterminado el rectángulo especificado (o predeterminado) por la \_ \_ \_ marca de vídeo de DGV de MCI Put para el comando [MCI \_ Put](mci-put.md) . Cuando se establece de manera diferente que el rectángulo de vídeo, lo que se muestra no es lo que se registra

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpRecord* apunta a una estructura [**parms de \_ \_ Registro \_ MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_ \_ grabación de VCR MCI \_ en
</dt> <dd>

El miembro **dwAt** de la estructura identificada por *lpRecord* contiene la hora a la que comienza el comando completo, o bien, si el dispositivo está preparado, cuando el dispositivo llega a la posición a partir del comando CUE.

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_ \_ inicialización del registro de VCR MCI \_
</dt> <dd>

Busque el dispositivo en el principio del medio, empiece a grabar vídeo y audio en blanco y grabe el código de tiempo, si es posible.

</dd> </dl>

En el caso de los dispositivos VCR, *lpRecord* apunta a una estructura [**\_ \_ \_ parms de registro VCR de MCI**](mci-vcr-record-parms.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

