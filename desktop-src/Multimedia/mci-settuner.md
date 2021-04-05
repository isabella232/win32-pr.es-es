---
title: Comando MCI_SETTUNER (mmsystem. h)
description: El \_ comando MCI SETTUNER establece el canal actual en el sintonizador. Los dispositivos VCR reconocen este comando.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- Comando de MCI_SETTUNER de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079749"
---
# <a name="mci_settuner-command"></a>\_Comando MCI SETTUNER

El \_ comando MCI SETTUNER establece el canal actual en el sintonizador. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*
</dt> <dd>

Puntero a una estructura de [**\_ \_ \_ parms VCR SETTUNER**](mci-vcr-settuner-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos VCR:

<dl> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_ \_ canal SETTUNER de VCR de MCI \_
</dt> <dd>

El miembro **dwChannel** de la estructura identificada por *lpSetTuner* contiene el nuevo número de canal.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>canal de SETTUNER de VCR de MCI \_ \_ \_ \_ inactivo
</dt> <dd>

Disminuye el canal del sintonizador.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_búsqueda de \_ canal de SETTUNER VCR \_ \_ de MCI \_
</dt> <dd>

Busca un canal válido en la dirección inversa.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_ \_ \_ \_ búsqueda de canal de SETTUNER VCR \_ de MCI
</dt> <dd>

Busca un canal válido en la dirección de avance.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_ \_ \_ canal \_ de SETTUNER de VCR de MCI up
</dt> <dd>

Incrementa el canal del sintonizador.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_ \_ número SETTUNER de VCR de MCI \_
</dt> <dd>

El miembro **dwNumber** de la estructura identificada por *lpSetTuner* especifica qué sintonizador lógico debe afectar a este comando.

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

 

