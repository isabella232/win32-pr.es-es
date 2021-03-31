---
title: Comando MCI_INFO (mmsystem. h)
description: El \_ comando MCI info recupera información de cadena de un dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- Comando de MCI_INFO de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150962"
---
# <a name="mci_info-command"></a>Comando de información de MCI \_

El \_ comando MCI info recupera información de cadena de un dispositivo. Todos los dispositivos reconocen este comando. La información se devuelve en el miembro **lpstrReturn** de la estructura identificada por *lpInfo*. El miembro **dwRetSize** especifica la longitud del búfer para los datos devueltos.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
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

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms**](mci-info-parms.md) de la información de MCI. (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La siguiente marca estándar adicional y específica del comando se aplica a todos los dispositivos que admiten la información de MCI \_ :

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_producto de información de MCI \_
</dt> <dd>

Obtiene una descripción del hardware asociado a un dispositivo. Los dispositivos deben proporcionar una descripción que identifique el controlador y el hardware utilizados.

</dd> </dl>

Las siguientes marcas adicionales se aplican al tipo de dispositivo **cdaudio** :

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>\_identidad de \_ medios de información de MCI \_
</dt> <dd>

Genera un identificador único para el CD de audio cargado actualmente en el reproductor que se consulta. Esta marca devuelve una cadena de 16 dígitos hexadecimales.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>\_UPC de \_ multimedia de información de MCI \_
</dt> <dd>

Genera el código universal de producto (UPC) que está codificado en un CD de audio. UPC es una cadena de dígitos. Es posible que no esté disponible para todos los CD.

</dd> </dl>

Las siguientes marcas adicionales se aplican al tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>elemento de información de MCI \_ DGV \_ \_
</dt> <dd>

Se incluye una constante que indica la información deseada en el miembro **dwItem** de la estructura identificada por *lpInfo*. Las siguientes constantes se definen para dispositivos de vídeo digital:

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>\_DGV de \_ audio de info \_ \_ de MCI
</dt> <dd>

Devuelve el nombre del algoritmo de compresión de audio actual.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ DGV \_ info \_ audio \_ Quality
</dt> <dd>

Devuelve el nombre del descriptor de calidad de audio actual.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>información de DGV de MCI \_ \_ \_ todavía \_ alg
</dt> <dd>

Devuelve el nombre del algoritmo de compresión de imagen fija actual.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>calidad de la información de MCI \_ DGV \_ \_ \_
</dt> <dd>

Devuelve el nombre del descriptor de calidad de imagen todavía actual.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>uso de información de MCI \_ DGV \_ \_
</dt> <dd>

Devuelve una cadena que describe las restricciones de uso que puede imponer el propietario de los datos visuales o sonoros en el área de trabajo.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>\_DGV de \_ vídeo de info \_ \_ de MCI
</dt> <dd>

Devuelve el nombre del algoritmo de compresión de vídeo actual.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>calidad de vídeo de MCI \_ DGV \_ info \_ \_
</dt> <dd>

Devuelve el nombre del descriptor de calidad de vídeo actual.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_versión de información de MCI \_
</dt> <dd>

Devuelve el nivel de versión del controlador de dispositivo y el hardware. Los desarrolladores de controladores de dispositivos deben documentar la sintaxis de la cadena devuelta.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>texto de información de MCI \_ DGV \_ \_
</dt> <dd>

Obtiene el título de la ventana.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_archivo de información de MCI \_
</dt> <dd>

Obtiene la ruta de acceso y el nombre del último archivo especificado con el comando [MCI \_ Open](mci-open.md) o [MCI \_ Load](mci-load.md) . Si no se ha especificado un archivo, el dispositivo devuelve una cadena terminada en NULL. Esta marca solo es compatible con dispositivos que devuelven **true** a la \_ marca MCI GETDEVCAPS \_ use \_ files del comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpInfo* apunta a una estructura [**MCI \_ DGV \_ info \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .

Las siguientes marcas adicionales se aplican al tipo de dispositivo **Sequencer** :

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>\_copyright de información de MCI \_
</dt> <dd>

Obtiene el aviso de copyright del archivo MIDI del evento meta de copyright.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_archivo de información de MCI \_
</dt> <dd>

Obtiene el nombre de archivo del archivo actual. Esta marca solo es compatible con los dispositivos que devuelven **true** cuando se llama al comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con la \_ marca MCI GETDEVCAPS \_ usa \_ files.

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>nombre de la información de MCI \_ \_
</dt> <dd>

Obtiene el nombre de secuencia del evento meta Sequence/Track Name.

</dd> </dl>

La marca adicional siguiente se aplica al tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_versión de \_ información de VCR de MCI \_
</dt> <dd>

Establece el miembro **lpstrReturn** de la estructura [**MCI \_ info \_ parms**](mci-info-parms.md) para que apunte al número de versión. También establece el miembro **dwRetSize** igual a la longitud de la cadena a la que se señala.

</dd> </dl>

Las siguientes marcas adicionales se aplican al tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_archivo de información de MCI \_
</dt> <dd>

Obtiene el nombre de archivo del archivo actual. Esta marca solo es compatible con dispositivos que devuelven **true** a la \_ marca MCI GETDEVCAPS \_ use \_ files del comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>texto de información de MCI \_ OVLY \_ \_
</dt> <dd>

Obtiene el título de la ventana asociada con el dispositivo de superposición de vídeo.

</dd> </dl>

Las siguientes marcas adicionales se aplican al tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_archivo de información de MCI \_
</dt> <dd>

Obtiene el nombre de archivo del archivo actual. Esta marca es compatible con los dispositivos que devuelven **true** cuando se llama al comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con la \_ marca MCI GETDEVCAPS \_ usa \_ files.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda de MCI \_
</dt> <dd>

Obtiene el nombre de producto de la entrada actual.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_salida de onda de MCI \_
</dt> <dd>

Obtiene el nombre de producto de la salida actual y su valor es específico del dispositivo.

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

 

