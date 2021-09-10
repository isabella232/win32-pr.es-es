---
title: MCI_LIST comando (Mmsystem.h)
description: El comando LIST de MCI obtiene información sobre el número y los \_ tipos de entradas disponibles para el dispositivo. Los dispositivos de vídeo digital y VCR reconocen este comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370033"
---
# <a name="mci_list-command"></a>Comando LIST de MCI \_

El comando LIST de MCI obtiene información sobre el número y los \_ tipos de entradas disponibles para el dispositivo. Los dispositivos de vídeo digital y VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
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

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican al tipo **de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ LIST \_ ALG
</dt> <dd>

El **miembro lpstrAlgorithm** de la estructura identificada por *lpList* contiene una dirección de un búfer que contiene el nombre de un algoritmo. El nombre se usa para recuperar los tipos de descriptores de calidad asociados a un algoritmo.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI \_ DGV \_ LIST \_ COUNT
</dt> <dd>

Devuelve el número de opciones del tipo especificado.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>ELEMENTO DE \_ LISTA MCI DGV \_ \_
</dt> <dd>

Una constante que indica el tipo de lista se incluye en el **miembro dwItem** de la estructura identificada por *lpList*. Esta marca es obligatoria. Use una de las siguientes constantes para indicar el tipo de lista:

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ ALG
</dt> <dd>

El comando debe recuperar los nombres de los algoritmos de audio.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ QUALITY
</dt> <dd>

El comando debe recuperar los niveles de calidad de audio. Los niveles devueltos están asociados al algoritmo al que hace referencia el **miembro lpstrAlgorithm** de la estructura identificada por *lpList*. Si ese miembro se especifica mediante la cadena "current", se devuelven las calidades asociadas al algoritmo actual.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>SECUENCIA DE \_ AUDIO DE LISTA DE MCI DGV \_ \_ \_
</dt> <dd>

El comando debe recuperar los nombres de las secuencias de audio.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI \_ DGV \_ LIST \_ STILL \_ AL
</dt> <dd>

El comando debe recuperar los nombres de los algoritmos still.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI \_ DGV \_ LIST \_ STILL \_ QUALITY
</dt> <dd>

El comando debe recuperar los niveles de calidad. Los niveles devueltos están asociados al algoritmo al que hace referencia el **miembro lpstrAlgorithm** de la estructura identificada por *lpList*. Si ese miembro se especifica mediante la cadena "current", se devuelven las calidades asociadas al algoritmo actual.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ ALG
</dt> <dd>

El comando debe recuperar nombres de algoritmos de vídeo.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ QUALITY
</dt> <dd>

El comando debe recuperar los niveles de calidad del vídeo. Los niveles devueltos están asociados al algoritmo al que hace referencia el **miembro lpstrAlgorithm** de la estructura identificada por *lpList*. Si ese miembro se especifica mediante la cadena "current", se devuelven las calidades asociadas al algoritmo actual.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>ORIGEN DE \_ VÍDEO DE LA LISTA DE MCI DGV \_ \_ \_
</dt> <dd>

El comando debe devolver información sobre los orígenes de vídeo. Cuando se usa con MCI \_ DGV \_ LIST \_ COUNT, el comando devuelve el número de orígenes de vídeo. Cuando se usa con MCI \_ DGV \_ LIST \_ NUMBER, el comando devuelve el tipo de un origen de vídeo. MCI define los siguientes tipos:

-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ GENERIC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ CIDE
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO

Puede haber más de un origen de cada tipo devuelto. El tipo de origen genérico se usa cuando se permite más de un tipo de señal para ese conector.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>SECUENCIA DE \_ VÍDEO DE LISTA DE MCI DGV \_ \_ \_
</dt> <dd>

El comando debe recuperar los nombres de las secuencias de vídeo.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>NÚMERO DE LISTA \_ DE MCI DGV \_ \_
</dt> <dd>

Se especifica un índice en el miembro **dwNumber** de la estructura identificada por *lpList*. El índice debe ser un entero entre 1 y el valor devuelto para la marca \_ MCI DGV \_ LIST \_ COUNT.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpList* apunta a una estructura [**\_ MCI DGV \_ LIST \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa)

Las marcas adicionales siguientes se aplican al tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>ORIGEN DE \_ AUDIO DE LA LISTA DE VCR \_ \_ DE \_ MCI
</dt> <dd>

Enumerar entradas o tipos de audio.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI \_ VCR \_ LIST \_ COUNT
</dt> <dd>

Establece el **miembro dwReturn** de la estructura identificada por *lpList* en el número total de entradas de audio o vídeo.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>NÚMERO DE LISTA \_ DE VCR \_ de MCI \_
</dt> <dd>

Establece el **miembro dwReturn** de la estructura identificada por *lpList* en el tipo de entrada de audio o vídeo especificado por el **miembro dwNumber.**

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>ORIGEN DE \_ VÍDEO DE LA LISTA DE VCR \_ \_ DE \_ MCI
</dt> <dd>

Enumera los tipos o entradas de vídeo.

</dd> </dl>

En el caso de los dispositivos VCR, *lpList* apunta a una estructura [**\_ MCI VCR \_ LIST \_ PARMS.**](mci-vcr-list-parms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 

