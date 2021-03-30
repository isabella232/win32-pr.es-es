---
title: Comando MCI_SEEK (mmsystem. h)
description: El \_ comando MCI Seek cambia la posición actual en el contenido lo más rápido posible.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- Comando de MCI_SEEK de Windows multimedia
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
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079061"
---
# <a name="mci_seek-command"></a>Comando de búsqueda de MCI \_

El \_ comando MCI Seek cambia la posición actual en el contenido lo más rápido posible. La salida de vídeo y audio se deshabilitan durante la búsqueda. Una vez finalizada la búsqueda, el dispositivo se detiene. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms de búsqueda de MCI**](mci-seek-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si un tamaño de muestra de datos para un dispositivo es mayor que 1 byte (por ejemplo, con datos estéreo de audio de onda), este comando se desplaza al principio del ejemplo más próximo cuando una posición especificada no coincide con el inicio de un ejemplo.

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ Seek:

<dl> <dt>

<span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>\_búsqueda \_ de MCI hasta el \_ final
</dt> <dd>

Busque el final del contenido.

</dd> <dt>

<span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>\_búsqueda \_ de MCI en \_ Start
</dt> <dd>

Busque el principio del contenido.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Se incluye una posición en el miembro **dwTo** de la estructura identificada por *lpSeek*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) . No use esta marca con MCI \_ Seek \_ to \_ End o MCI \_ Seek \_ to \_ Start.

</dd> </dl>

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>\_ \_ búsqueda de VCR \_ de MCI en
</dt> <dd>

El miembro **dwAt** de la estructura identificada por *lpSeek* contiene la hora a la que comienza el comando completo.

</dd> <dt>

<span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_marca de \_ búsqueda de VCR MCI \_
</dt> <dd>

El miembro **dwMark** de la estructura identificada por *lpSeek* contiene la marca numerada que se va a buscar.

</dd> <dt>

<span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>búsqueda de VCR de MCI \_ \_ \_ inversa
</dt> <dd>

La dirección de búsqueda es inversa; solo se usa con la marca de \_ búsqueda de vídeo de MCI \_ \_ .

</dd> </dl>

En el caso de los dispositivos VCR, el parámetro *lpSeek* apunta a una estructura [**parms de búsqueda de VCR de MCI \_ \_ \_**](mci-vcr-seek-parms.md) .

La siguiente marca adicional se usa con el tipo de dispositivo de **videodisco** :

<dl> <dt>

<span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>búsqueda de MCI \_ Vd \_ \_ inverso
</dt> <dd>

La dirección de búsqueda es inversa.

</dd> </dl>

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

 

