---
title: MCI_SEEK comando (Mmsystem.h)
description: El comando \_ MCI SEEK cambia la posición actual del contenido lo antes posible.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- MCI_SEEK comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d901bf92e3495dde9a16e7499dcaae850b5e50eab2b4df1af99ca39f290cc981
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430485"
---
# <a name="mci_seek-command"></a>Comando \_ MCI SEEK

El comando \_ MCI SEEK cambia la posición actual del contenido lo antes posible. La salida de audio y vídeo se deshabilita durante la búsqueda. Una vez completada la búsqueda, el dispositivo se detiene. Los dispositivos cd audio, digital-video, secuenciador MIDI, VCR, videodisc y audio de forma de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
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

<span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*
</dt> <dd>

Puntero a una [**estructura \_ MCI SEEK \_ PARMS.**](mci-seek-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si un tamaño de muestra de datos para un dispositivo es superior a 1 byte (por ejemplo, con datos estéreo de audio de forma de onda), este comando se mueve al principio de la muestra más cercana cuando una posición especificada no coincide con el inicio de una muestra.

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ SEEK:

<dl> <dt>

<span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI \_ SEEK \_ TO \_ END
</dt> <dd>

Busque hasta el final del contenido.

</dd> <dt>

<span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ SEEK \_ TO \_ START
</dt> <dd>

Busque al principio del contenido.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye una posición en el **miembro dwTo** de la estructura identificada *por lpSeek*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md) No use esta marca con MCI \_ SEEK TO END o \_ \_ MCI SEEK TO \_ \_ \_ START.

</dd> </dl>

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI \_ VCR \_ SEEK \_ AT
</dt> <dd>

El **miembro dwAt** de la estructura identificada por *lpSeek* contiene una hora en la que comienza todo el comando.

</dd> <dt>

<span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI \_ VCR \_ SEEK \_ MARK
</dt> <dd>

El **miembro dwMark** de la estructura identificada por *lpSeek* contiene la marca numerada que se debe buscar.

</dd> <dt>

<span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI \_ VCR \_ SEEK \_ REVERSE
</dt> <dd>

La dirección de búsqueda es inversa; solo se usa con la marca \_ MCI VCR \_ SEEK \_ MARK.

</dd> </dl>

En el caso de los dispositivos VCR, el *parámetro lpSeek* apunta a una estructura [**\_ MCI VCR \_ SEEK \_ PARMS.**](mci-vcr-seek-parms.md)

La siguiente marca adicional se usa con el **tipo de dispositivo videodisc:**

<dl> <dt>

<span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI \_ VD \_ SEEK \_ REVERSE
</dt> <dd>

La dirección de la búsqueda es inversa.

</dd> </dl>

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

 

