---
title: MCI_INFO comando (Mmsystem.h)
description: El comando INFO de MCI \_ recupera información de cadena de un dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO comando Windows Multimedia
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
ms.openlocfilehash: 18d53acbdfeb0c13b4b9e201d1bea23008dfbaa83221007152181fe685d09957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039205"
---
# <a name="mci_info-command"></a>Comando INFO de MCI \_

El comando INFO de MCI \_ recupera información de cadena de un dispositivo. Todos los dispositivos reconocen este comando. Se devuelve información en el **miembro lpstrReturn** de la estructura identificada por *lpInfo*. El **miembro dwRetSize** especifica la longitud del búfer para los datos devueltos.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital y VCR, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

Puntero a una [**estructura \_ MCI INFO \_ PARMS.**](mci-info-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

La siguiente marca estándar adicional y específica del comando se aplica a todos los dispositivos que admiten MCI \_ INFO:

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>PRODUCTO DE \_ INFORMACIÓN DE \_ MCI
</dt> <dd>

Obtiene una descripción del hardware asociado a un dispositivo. Los dispositivos deben proporcionar una descripción que identifique tanto el controlador como el hardware usado.

</dd> </dl>

Las siguientes marcas adicionales se aplican al tipo **de dispositivo cdaudio:**

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI \_ INFO \_ MEDIA \_ IDENTITY
</dt> <dd>

Genera un identificador único para el CD de audio cargado actualmente en el reproductor que se está consultando. Esta marca devuelve una cadena de 16 dígitos hexadecimales.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>UPC de MCI \_ INFO \_ \_ MEDIA
</dt> <dd>

Genera el código de producto universal (UPC) codificado en un CD de audio. El UPC es una cadena de dígitos. Es posible que no esté disponible para todos los CDs.

</dd> </dl>

Las siguientes marcas adicionales se aplican al tipo **de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>ELEMENTO DE INFORMACIÓN \_ DE MCI DGV \_ \_
</dt> <dd>

Una constante que indica la información deseada se incluye en el **miembro dwItem** de la estructura identificada por *lpInfo*. Las siguientes constantes se definen para dispositivos de vídeo digital:

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ INFO \_ AUDIO \_ ALG
</dt> <dd>

Devuelve el nombre del algoritmo de compresión de audio actual.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>CALIDAD DE \_ AUDIO DE MCI DGV \_ \_ \_ INFO
</dt> <dd>

Devuelve el nombre del descriptor de calidad de audio actual.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI \_ DGV \_ INFO \_ STILL \_ ALG
</dt> <dd>

Devuelve el nombre del algoritmo de compresión de imagen todavía actual.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI \_ DGV \_ INFO \_ STILL \_ QUALITY
</dt> <dd>

Devuelve el nombre del descriptor de calidad de imagen todavía actual.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>USO DE INFORMACIÓN \_ DE MCI DGV \_ \_
</dt> <dd>

Devuelve una cadena que describe las restricciones de uso que podría imponer el propietario de los datos visuales o visuales en el área de trabajo.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>VÍDEO DE \_ INFORMACIÓN DE MCI DGV \_ \_ \_ ALG
</dt> <dd>

Devuelve el nombre del algoritmo de compresión de vídeo actual.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>CALIDAD DE VÍDEO \_ DE INFORMACIÓN DE MCI DGV \_ \_ \_
</dt> <dd>

Devuelve el nombre del descriptor de calidad de vídeo actual.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>VERSIÓN DE INFORMACIÓN DE MCI \_ \_
</dt> <dd>

Devuelve el nivel de versión del controlador y el hardware del dispositivo. Los desarrolladores de controladores de dispositivos deben documentar la sintaxis de la cadena devuelta.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>TEXTO DE INFORMACIÓN \_ DE MCI DGV \_ \_
</dt> <dd>

Obtiene el título de la ventana.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>ARCHIVO DE \_ INFORMACIÓN DE \_ MCI
</dt> <dd>

Obtiene la ruta de acceso y el nombre de archivo del último archivo especificado con el [comando MCI \_ OPEN](mci-open.md) [o MCI \_ LOAD.](mci-load.md) Si no se ha especificado un archivo, el dispositivo devuelve una cadena terminada en NULL. Esta marca solo es compatible con dispositivos que devuelven **TRUE** a la marca \_ MCI GETDEVCAPS USA FILES del comando \_ \_ [ \_ GETDEVCAPS de MCI.](mci-getdevcaps.md)

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpInfo* apunta a una estructura [**\_ MCI DGV \_ INFO \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa)

Las marcas adicionales siguientes se aplican al **tipo de dispositivo sequencer:**

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>DERECHOS DE AUTOR DE LA INFORMACIÓN DE MCI \_ \_
</dt> <dd>

Obtiene el aviso de copyright del archivo MIDI del meta evento de copyright.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>ARCHIVO DE \_ INFORMACIÓN DE \_ MCI
</dt> <dd>

Obtiene el nombre de archivo del archivo actual. Esta marca solo es compatible con dispositivos que **devuelven TRUE** cuando se llama al comando [ \_ GETDEVCAPS](mci-getdevcaps.md) de MCI con la marca \_ MCI GETDEVCAPS \_ USA \_ ARCHIVOS.

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>NOMBRE DE INFORMACIÓN DE MCI \_ \_
</dt> <dd>

Obtiene el nombre de secuencia del meta event de nombre de secuencia o pista.

</dd> </dl>

La siguiente marca adicional se aplica al tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>VERSIÓN DE \_ INFORMACIÓN DE VCR \_ DE MCI \_
</dt> <dd>

Establece **el miembro lpstrReturn** de la [**estructura \_ MCI INFO \_ PARMS**](mci-info-parms.md) para que apunte al número de versión. También establece el **miembro dwRetSize** igual a la longitud de la cadena a la que se apunta.

</dd> </dl>

Las marcas adicionales siguientes se aplican al tipo **de dispositivo de** superposición:

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>ARCHIVO DE \_ INFORMACIÓN DE \_ MCI
</dt> <dd>

Obtiene el nombre de archivo del archivo actual. Esta marca solo es compatible con dispositivos que devuelven **TRUE** a la marca \_ MCI GETDEVCAPS USA FILES del comando \_ \_ [ \_ GETDEVCAPS de MCI.](mci-getdevcaps.md)

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>TEXTO DE INFORMACIÓN DE MCI \_ \_ \_ OVLY
</dt> <dd>

Obtiene el título de la ventana asociada al dispositivo de superposición de vídeo.

</dd> </dl>

Las siguientes marcas adicionales se aplican al tipo **de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>ARCHIVO DE \_ INFORMACIÓN DE \_ MCI
</dt> <dd>

Obtiene el nombre de archivo del archivo actual. Esta marca es compatible con los dispositivos que devuelven **TRUE** cuando se llama al comando [ \_ GETDEVCAPS](mci-getdevcaps.md) de MCI con la marca \_ MCI GETDEVCAPS \_ USA \_ FILES.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>ENTRADA DE \_ MCI WAVE \_
</dt> <dd>

Obtiene el nombre del producto de la entrada actual.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>SALIDA DE MCI \_ WAVE \_
</dt> <dd>

Obtiene el nombre del producto de la salida actual y su valor es específico del dispositivo.

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

 

