---
title: MCI_UNFREEZE comando (Mmsystem.h)
description: El comando UNFREEZE de MCI restaura el movimiento en un área del búfer de vídeo \_ inmovilizado con el comando MCI \_ FREEZE. Los dispositivos de vídeo digital, VCR y superposición de vídeo reconocen este comando.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370184"
---
# <a name="mci_unfreeze-command"></a>Comando \_ MCI UNFREEZE

El comando UNFREEZE de MCI restaura el movimiento en un área del búfer de vídeo \_ inmovilizado con el [comando MCI \_ FREEZE.](mci-freeze.md) Los dispositivos de vídeo digital, VCR y superposición de vídeo reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
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

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

La siguiente marca adicional se usa con el **tipo de dispositivo digitalvideo:**

MCI \_ DGV \_ RECT

El **miembro rc** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido. El rectángulo especifica una región dentro del búfer de marco cuyos píxeles deben tener desactivado su bit de máscara de bloqueo. Las regiones rectangulares se especifican como se describe para el [comando \_ PUT de MCI.](mci-put.md) Si se omite, el rectángulo tiene como valor predeterminado todo el búfer de fotogramas. Mediante el uso de una secuencia de comandos inmovilizar y descongelar con rectángulos diferentes, se pueden describir patrones arbitrarios de bits de máscara de bloqueo.

En el caso de los dispositivos de vídeo digital, el parámetro *lpUnfreeze* apunta a una estructura **\_ MCI DGV \_ UNFREEZE \_ PARMS.** Para más información, consulte los comentarios de la estructura [**\_ MCI DGV \_ RECT \_ PARMS.**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>ENTRADA MCI \_ VCR \_ \_ UNFREEZE
</dt> <dd>

Descongele la entrada.

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>SALIDA DE \_ DESCONGELAR VCR \_ DE MCI \_
</dt> <dd>

Descongele la salida.

</dd> </dl>

La siguiente marca adicional se usa con el tipo **de dispositivo de** superposición:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido. Es un parámetro obligatorio.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpUnfreeze* apunta a una estructura [**\_ MCI OVLY \_ RECT \_ PARMS.**](mci-ovly-rect-parms.md)

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

 

