---
title: MCI_SETTUNER comando (Mmsystem.h)
description: El comando SETTUNER de MCI \_ establece el canal actual en el afinador. Los dispositivos VCR reconocen este comando.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- MCI_SETTUNER comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc0e4d812a89c8b7ca5a8e65b322e19dcb4f7d4e7e2ef8c49745ebb16e22af65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138111"
---
# <a name="mci_settuner-command"></a>Comando \_ SETTUNER de MCI

El comando SETTUNER de MCI \_ establece el canal actual en el afinador. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
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

<span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*
</dt> <dd>

Puntero a una [**estructura \_ MCI VCR \_ SETTUNER \_ PARMS.**](mci-vcr-settuner-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

Las siguientes marcas adicionales se aplican a los dispositivos VCR:

<dl> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL
</dt> <dd>

El **miembro dwChannel** de la estructura identificada por *lpSetTuner* contiene el nuevo número de canal.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ DOWN
</dt> <dd>

Disminuye el canal del tuner.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ SEEK \_ DOWN
</dt> <dd>

Busca un canal válido en la dirección inversa.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ SEEK \_ UP
</dt> <dd>

Busca un canal válido en la dirección hacia delante.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ UP
</dt> <dd>

Incrementa el canal de tuner.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI \_ VCR \_ SETTUNER \_ NUMBER
</dt> <dd>

El **miembro dwNumber** de la estructura identificada por *lpSetTuner* especifica qué afinador lógico se debe afectar con este comando.

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

 

