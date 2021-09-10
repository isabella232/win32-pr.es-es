---
title: MCI_SETTUNER comando (Mmsystem.h)
description: El comando SETTUNER de MCI \_ establece el canal actual en el ajuste. Los dispositivos VCR reconocen este comando.
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
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370094"
---
# <a name="mci_settuner-command"></a>Comando \_ SETTUNER de MCI

El comando SETTUNER de MCI \_ establece el canal actual en el ajuste. Los dispositivos VCR reconocen este comando.

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

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos VCR:

<dl> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>CANAL \_ SETTUNER DE MCI VCR \_ \_
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

Busca un canal válido en la dirección de avance.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ UP
</dt> <dd>

Incrementa el canal del tuner.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI \_ VCR \_ SETTUNER \_ NUMBER
</dt> <dd>

El **miembro dwNumber** de la estructura identificada por *lpSetTuner* especifica qué afinador lógico debe afectar con este comando.

</dd> </dl>

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

 

