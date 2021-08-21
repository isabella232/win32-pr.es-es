---
title: MCI_QUALITY comando (Mmsystem.h)
description: El comando MCI QUALITY define un nivel de calidad personalizado para la compresión de \_ datos de audio, vídeo o imagen fija. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1237d9b70c9f06782342c404c19dd23cf6f0848f8c7b33523bce35990287fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138226"
---
# <a name="mci_quality-command"></a>Comando MCI \_ QUALITY

El comando MCI QUALITY define un nivel de calidad personalizado para la compresión de \_ datos de audio, vídeo o imagen fija. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
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

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

Puntero a una [**estructura \_ MCI DGV \_ QUALITY \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

El nombre definido para este nivel de calidad se puede usar al establecer el audio, el vídeo o la calidad con los comandos [MCI \_ SETAUDIO](mci-setaudio.md) y [MCI \_ SETVIDEO.](mci-setvideo.md)

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ QUALITY \_ ALG
</dt> <dd>

El **miembro lpstrAlgorithm** de la estructura identificada por *lpQuality* contiene una dirección de un búfer que contiene el nombre del algoritmo. Este algoritmo debe ser compatible con el controlador del dispositivo y debe ser compatible con el descriptor de audio, still o vídeo que se usa. Si se omite esta marca, se usa el algoritmo actual.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>CUADRO DE DIÁLOGO CALIDAD DE MCI \_ \_
</dt> <dd>

El controlador de dispositivo debe mostrar un cuadro de diálogo para especificar el nivel de calidad. El cuadro de diálogo tiene campos específicos del algoritmo usados internamente por el controlador de dispositivo para crear una estructura que describa un nivel de calidad específico.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>IDENTIFICADOR DE CALIDAD DE MCI \_ \_
</dt> <dd>

El **miembro dwHandle** de la estructura identificada por *lpQuality* contiene un identificador para una estructura. La estructura contiene datos específicos del algoritmo que describen el nivel de calidad específico. El formato de las estructuras de los algoritmos depende del dispositivo.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>ELEMENTO DE CALIDAD DE MCI \_ \_
</dt> <dd>

Una constante que indica el tipo de algoritmo se incluye en el **miembro dwItem** de la estructura identificada *por lpQuality*.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>NOMBRE DE CALIDAD DE MCI \_ \_
</dt> <dd>

El **miembro lpstrName** de la estructura identificada por *lpQuality* contiene una dirección de un búfer que contiene el descriptor de calidad.

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

 

