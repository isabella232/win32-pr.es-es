---
title: Comando MCI_QUALITY (mmsystem. h)
description: El \_ comando MCI Quality define un nivel de calidad personalizado para la compresión de datos de audio, vídeo o imagen fija. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- Comando de MCI_QUALITY de Windows multimedia
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
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421911"
---
# <a name="mci_quality-command"></a>Comando de calidad de MCI \_

El \_ comando MCI Quality define un nivel de calidad personalizado para la compresión de datos de audio, vídeo o imagen fija. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

Puntero a una estructura de [**\_ \_ \_ parms de calidad DGV de MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El nombre definido para este nivel de calidad se puede usar al establecer el audio, el vídeo o la calidad continua con los comandos [MCI \_ SETAUDIO](mci-setaudio.md) y [MCI \_ SETVIDEO](mci-setvideo.md) .

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>\_alg calidad de MCI \_
</dt> <dd>

El miembro **lpstrAlgorithm** de la estructura identificada por *lpQuality* contiene una dirección de un búfer que contiene el nombre del algoritmo. Este algoritmo debe ser compatible con el controlador de dispositivo y debe ser compatible con el descriptor de vídeo, de audio o de vídeo que se usa. Si se omite esta marca, se utiliza el algoritmo actual.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_cuadro de diálogo calidad de MCI \_
</dt> <dd>

El controlador de dispositivo debe mostrar un cuadro de diálogo para especificar el nivel de calidad. El cuadro de diálogo tiene campos específicos del algoritmo utilizados internamente por el controlador de dispositivo para crear una estructura que describe un nivel de calidad específico.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_controlador de calidad de MCI \_
</dt> <dd>

El miembro **dwHandle** de la estructura identificada por *lpQuality* contiene un identificador para una estructura. La estructura contiene datos específicos del algoritmo que describen el nivel de calidad específico. El formato de las estructuras para los algoritmos depende del dispositivo.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_elemento de calidad de MCI \_
</dt> <dd>

Una constante que indica el tipo de algoritmo se incluye en el miembro **dwItem** de la estructura identificada por *lpQuality*.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_nombre de calidad de MCI \_
</dt> <dd>

El miembro **lpstrName** de la estructura identificada por *lpQuality* contiene una dirección de un búfer que contiene el descriptor de calidad.

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

 

