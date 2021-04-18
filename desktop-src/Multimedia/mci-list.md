---
title: Comando MCI_LIST (mmsystem. h)
description: El \_ comando MCI List obtiene información sobre el número y los tipos de entradas disponibles para el dispositivo. Los dispositivos digitales-vídeo y VCR reconocen este comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- Comando de MCI_LIST de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535422"
---
# <a name="mci_list-command"></a>\_Comando de lista MCI

El \_ comando MCI List obtiene información sobre el número y los tipos de entradas disponibles para el dispositivo. Los dispositivos digitales-vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican al tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>\_DGV de \_ lista de MCI \_
</dt> <dd>

El miembro **lpstrAlgorithm** de la estructura identificada por *lpList* contiene una dirección de un búfer que contiene el nombre de un algoritmo. El nombre se utiliza para recuperar los tipos de descriptores de calidad asociados a un algoritmo.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>recuento de listas de DGV de MCI \_ \_ \_
</dt> <dd>

Devuelve el número de opciones del tipo especificado.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_elemento de \_ lista \_ DGV de MCI
</dt> <dd>

Una constante que indica que el tipo de lista se incluye en el miembro **dwItem** de la estructura identificada por *lpList*. Esta marca es obligatoria. Use una de las siguientes constantes para indicar el tipo de lista:

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>\_DGV de \_ audio de lista \_ \_ de MCI
</dt> <dd>

El comando debe recuperar los nombres de los algoritmos de audio.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ lista \_ de \_ calidad de audio
</dt> <dd>

El comando debe recuperar los niveles de calidad de audio. Los niveles devueltos están asociados al algoritmo al que hace referencia el miembro **lpstrAlgorithm** de la estructura identificada por *lpList*. Si ese miembro se especifica mediante la cadena "actual", se devuelven las cualidades asociadas al algoritmo actual.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_secuencia de \_ audio de lista DGV \_ de MCI \_
</dt> <dd>

El comando debe recuperar los nombres de las secuencias de audio.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>lista de DGV de MCI \_ \_ \_ todavía \_ al
</dt> <dd>

El comando debe recuperar los nombres de los algoritmos de todavía.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>calidad de la \_ lista de DGV MCI \_ \_ \_
</dt> <dd>

El comando debe recuperar los niveles de calidad. Los niveles devueltos están asociados al algoritmo al que hace referencia el miembro **lpstrAlgorithm** de la estructura identificada por *lpList*. Si ese miembro se especifica mediante la cadena "actual", se devuelven las cualidades asociadas al algoritmo actual.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>\_vídeo de \_ vídeo de lista de DGV MCI \_ \_
</dt> <dd>

El comando debe recuperar los nombres de los algoritmos de vídeo.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_calidad de \_ vídeo de lista DGV \_ de MCI \_
</dt> <dd>

El comando debe recuperar los niveles de calidad de vídeo. Los niveles devueltos están asociados al algoritmo al que hace referencia el miembro **lpstrAlgorithm** de la estructura identificada por *lpList*. Si ese miembro se especifica mediante la cadena "actual", se devuelven las cualidades asociadas al algoritmo actual.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_origen de \_ vídeo de lista de DGV de MCI \_ \_
</dt> <dd>

El comando debe devolver información sobre los orígenes de vídeo. Cuando se usa con \_ \_ \_ el recuento de lista de DGV de MCI, el comando devuelve el número de orígenes de vídeo. Cuando se usa con \_ \_ \_ el número de lista DGV de MCI, el comando devuelve el tipo de un origen de vídeo. MCI define los siguientes tipos:

-   MCI \_ DGV \_ SETVIDEO \_ src \_ Generic
-   MCI \_ DGV \_ SETVIDEO \_ src \_ NTSC
-   MCI \_ DGV \_ SETVIDEO \_ src \_ PAL
-   MCI \_ DGV \_ SETVIDEO \_ src \_ RGB
-   MCI \_ DGV \_ SETVIDEO \_ src \_ SECAM
-   MCI \_ DGV \_ SETVIDEO \_ src \_ Svideo

Puede haber más de un origen de cada tipo devuelto. El tipo de origen genérico se usa cuando se permite más de un tipo de señal para dicho conector.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_secuencia de \_ vídeo de lista de DGV MCI \_ \_
</dt> <dd>

El comando debe recuperar los nombres de las secuencias de vídeo.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_número de \_ lista de DGV de MCI \_
</dt> <dd>

Se especifica un índice en el miembro **dwNumber** de la estructura identificada por *lpList*. El índice debe ser un entero comprendido entre 1 y el valor devuelto para \_ la \_ marca de recuento de lista MCI DGV \_ .

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpList* apunta a una estructura [**parms de MCI \_ DGV \_ List \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .

Las siguientes marcas adicionales se aplican al tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_origen de \_ audio de lista de VCR de MCI \_ \_
</dt> <dd>

Enumerar entradas o tipos de audio.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>recuento de lista de VCR de MCI \_ \_ \_
</dt> <dd>

Establece el miembro **dwReturn** de la estructura identificada por *lpList* en el número total de entradas de vídeo o audio.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>número de la \_ lista de VCR MCI \_ \_
</dt> <dd>

Establece el miembro **dwReturn** de la estructura identificada por *lpList* en el tipo de la entrada de vídeo o audio especificada por el miembro **dwNumber** .

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_origen de \_ vídeo de lista de VCR de MCI \_ \_
</dt> <dd>

Enumerar entradas o tipos de vídeo.

</dd> </dl>

En el caso de los dispositivos VCR, *lpList* apunta a una estructura de [**\_ \_ \_ parms de VCR de MCI**](mci-vcr-list-parms.md) .

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

 

