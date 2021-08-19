---
title: MCI_RECORD comando (Mmsystem.h)
description: El comando MCI \_ RECORD inicia la grabación desde la posición actual o desde una ubicación especificada a otra ubicación especificada.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- MCI_RECORD comando Windows Multimedia
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
ms.openlocfilehash: 327b9ed9b138b581bec17d8bfcfe19ae67bb07d59be2781af54e22a85e2133c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803456"
---
# <a name="mci_record-command"></a>Comando MCI \_ RECORD

El [**comando MCI \_ RECORD**](mci-record-parms.md) inicia la grabación desde la posición actual o desde una ubicación especificada a otra ubicación especificada. Los dispositivos VCR y de audio de forma de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores DE MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital y VCR, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*
</dt> <dd>

Puntero a una [**estructura MCI \_ RECORD \_ PARMS.**](mci-record-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Este comando es compatible con los dispositivos que devuelven **TRUE** cuando se llama al comando [ \_ GETDEVCAPS](mci-getdevcaps.md) de MCI con la marca \_ MCI GETDEVCAPS \_ CAN \_ RECORD. Para el controlador MCIWAVE, todos los datos registrados después de abrir un archivo se descartan si el archivo se cierra sin guardarlo.

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ RECORD:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Se incluye una ubicación inicial en el **miembro dwFrom** de la estructura identificada por *lpRecord*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md) Si no se especifica MCI FROM, la ubicación inicial tiene como valor predeterminado \_ la posición actual.

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>INSERCIÓN DE REGISTROS DE MCI \_ \_
</dt> <dd>

La información recién registrada debe insertarse o pegarse en los datos existentes. Es posible que algunos dispositivos no lo admitan. Si se admite, este es el valor predeterminado.

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>\_SOBRESCRITURA DE REGISTROS MCI \_
</dt> <dd>

Los datos deben sobrescribir los datos existentes. The MCIWAVE. El dispositivo DRV devuelve MCIERR \_ UNSUPPORTED \_ FUNCTION en respuesta a esta marca.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye una ubicación final en el **miembro dwTo** de la estructura identificada por *lpRecord*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md) Si no se especifica MCI TO, la ubicación final tiene como valor predeterminado \_ el final del contenido.

</dd> </dl>

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>SECUENCIA DE \_ AUDIO DE GRABACIÓN DE MCI DGV \_ \_ \_
</dt> <dd>

Se incluye un número de secuencia de audio en el **miembro dwAudioStream** de la estructura identificada *por lpRecord*. Si omite esta marca, los datos de audio se graban en la primera secuencia física.

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>RETENCIÓN DE \_ REGISTROS DE MCI DGV \_ \_
</dt> <dd>

Cuando se detenga la grabación, la pantalla contendrá la última imagen y no se reanudará mostrando el vídeo hasta que se emita un comando monitor de [MCI. \_ ](mci-monitor.md)

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>SECUENCIA DE \_ VÍDEO DE GRABACIÓN DE MCI DGV \_ \_ \_
</dt> <dd>

Se incluye un número de secuencia de vídeo en el **miembro dwVideoStream** de la estructura identificada *por lpRecord*. Si omite esta marca, los datos de vídeo se graban en la primera secuencia física.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

Se especifica un rectángulo en el miembro **rc** de la estructura identificada por *lpRecord*. El rectángulo especifica la región de la entrada externa utilizada como origen de los píxeles comprimidos y guardados. Este rectángulo tiene como valor predeterminado el rectángulo especificado (o predeterminado) por la marca PUT VIDEO de MCI DGV para \_ \_ el comando PUT \_ [ \_ de MCI.](mci-put.md) Cuando se establece de forma diferente que el rectángulo de vídeo, lo que se muestra no es lo que se graba

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpRecord* apunta a una estructura [**\_ MCI DGV \_ RECORD \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>REGISTRO DE VCR DE MCI \_ \_ \_ EN
</dt> <dd>

El **miembro dwAt** de la estructura identificada por *lpRecord* contiene una hora en la que comienza todo el comando, o si el dispositivo es cued, cuando el dispositivo alcanza la posición desde dada por el comando cue.

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>INICIALIZACIÓN DEL \_ REGISTRO DE VCR \_ DE MCI \_
</dt> <dd>

Busque el dispositivo al principio del medio, comience a grabar vídeo y audio en blanco y, si es posible, registre el código de tiempo.

</dd> </dl>

En el caso de los dispositivos *VCR, lpRecord* apunta a una estructura [**\_ MCI VCR \_ RECORD \_ PARMS.**](mci-vcr-record-parms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 

