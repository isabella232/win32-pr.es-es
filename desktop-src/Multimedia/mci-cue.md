---
title: Comando MCI_CUE (mmsystem. h)
description: El \_ comando MCI CUE señala un dispositivo para que la reproducción o grabación comience con un retraso mínimo. Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- Comando de MCI_CUE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676862"
---
# <a name="mci_cue-command"></a>\_Comando MCI CUE

El \_ comando MCI CUE señala un dispositivo para que la reproducción o grabación comience con un retraso mínimo. Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
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

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_entrada de \_ indicación MCI DGV \_
</dt> <dd>

Una instancia de vídeo digital debe prepararse para la grabación. Si la aplicación no ha reservado espacio en disco, el dispositivo reserva el espacio en disco con sus parámetros predeterminados. La aplicación puede omitir esta marca si el origen de presentación actual ya es la entrada externa. (Esta marca no tiene ningún efecto en la selección del origen de presentación).

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>DGV de la señal de MCI \_ \_ \_
</dt> <dd>

Una instancia de vídeo digital debe prepararse para reproducir el marco especificado con el comando sin mostrarlo. Cuando se especifica esta marca, la pantalla continúa mostrando la imagen en el búfer de fotogramas aunque su fotograma correspondiente no sea la posición actual. Por ejemplo, si el búfer de fotogramas contiene la imagen del fotograma 7, el dispositivo continúa mostrando el fotograma 7 cuando se usa esta marca para señalar el dispositivo a cualquier otra posición. Un comando de pila subsiguiente sin esta marca y sin la \_ marca MCI to muestra el marco actual.

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>salida de indicación de MCI \_ DGV \_ \_
</dt> <dd>

Una instancia de vídeo digital debe prepararse para la reproducción. Si el área de trabajo está en pausa, no se produce ninguna posición. Si el área de trabajo está detenida, la posición puede cambiar a una imagen de fotograma clave anterior. La aplicación puede omitir esta marca si el origen de presentación actual ya es el área de trabajo.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Una posición en el área de trabajo se incluye en el miembro **dwTo** de la estructura identificada por *lpCue*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo de conjunto de MCI del comando [ \_ set de MCI](mci-set.md) . Esto es equivalente a buscar en una posición, excepto que el dispositivo se pausa después del comando.

</dd> </dl>

En el caso de los dispositivos **DigitalVideo** , el parámetro *lpCue* apunta a una estructura de parms de DGV de la [**\_ \_ señal \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde
</dt> <dd>

El miembro **dwFrom** de la estructura a la que apunta *lpCue* contiene la ubicación de inicio especificada en el formato de hora actual.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

El miembro **dwTo** de la estructura a la que apunta *lpCue* contiene la ubicación final (en pausa) especificada en el formato de hora actual.

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_entrada de \_ pista de VCR de MCI \_
</dt> <dd>

Preparación para la grabación.

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>salida de la señal de VCR de MCI \_ \_ \_
</dt> <dd>

Preparación para la reproducción. Si \_ \_ \_ no se especifica ninguna entrada de pila de VCR de MCI ni \_ \_ salida de señal de VCR MCI \_ , \_ \_ se presupone la salida de la señal de VCR de MCI \_ .

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>prelanzamiento de pista de VCR de MCI \_ \_ \_
</dt> <dd>

Señale el dispositivo a la posición actual, o la posición **dwFrom** , menos la duración del preroll. Esto permitirá que el dispositivo se prepare antes de entrar en el modo de grabación o reproducción.

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>pista de VCR de MCI \_ \_ \_ inverso
</dt> <dd>

La dirección del comando siguiente reproducir o grabar es inversa.

</dd> </dl>

Cuando cueing para la reproducción mediante el uso del \_ comando MCI CUE con la marca de salida de la \_ señal de VCR MCI \_ \_ , puede cancelar \_ la pila de MCI emitiendo el comando de [ \_ reproducción de MCI](mci-play.md) con MCI \_ de, MCI \_ a o MCI \_ VCR \_ Play \_ REVERSE.

Cuando cueing para la grabación mediante el uso de \_ la señal de MCI con la marca de entrada de vídeo de MCI \_ \_ \_ , puede cancelar \_ la señal de MCI emitiendo el comando [MCI \_ Record](mci-record.md) con MCI \_ de, MCI \_ a o el registro de VCR de MCI \_ \_ \_ Initialize.

En el caso de los dispositivos **VCR** , el parámetro *lpCue* apunta a una estructura [**MCI \_ VCR \_ CUE \_ parms**](mci-vcr-cue-parms.md) .

Con el tipo de dispositivo **WaveAudio** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda de MCI \_
</dt> <dd>

Un dispositivo de entrada de onda-audio debe estar preparado.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_salida de onda de MCI \_
</dt> <dd>

Un dispositivo de salida de onda-audio debe estar preparado. Esta es la marca predeterminada si no se especifica una marca.

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

 

