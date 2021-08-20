---
title: MCI_FREEZE comando (Mmsystem.h)
description: El comando MCI \_ FREEZE inmoviliza el movimiento en la pantalla. Los dispositivos de vídeo digital, superposición de vídeo y VCR reconocen este comando.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- MCI_FREEZE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc0d57daaa488d70654b946115264fc2177b959f73cbbcee1759bd6823bfaf4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986666"
---
# <a name="mci_freeze-command"></a>Comando MCI \_ FREEZE

El comando MCI \_ FREEZE inmoviliza el movimiento en la pantalla. Los dispositivos de vídeo digital, superposición de vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
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

<span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con parámetros adicionales podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

El tipo de dispositivo **digitalvideo** usa las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI \_ DGV \_ FREEZE \_ AT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpFreeze* contiene un rectángulo válido. El rectángulo especifica una región dentro del búfer de marco que tendrá activado el bit de máscara de bloqueo para cada píxel. Los píxeles especificados no se actualizarán hasta que se apague su bit de máscara de bloqueo. Si no se especifica esta marca, el rectángulo tiene como valor predeterminado todo el búfer de fotogramas. Esta marca solo se admite si el comando [ \_ GETDEVCAPS](mci-getdevcaps.md) de MCI devuelve **TRUE** para la marca \_ \_ GETDEVCAPS CAN LOCK de MCI \_ DGV. \_

</dd> <dt>

<span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>INMOVILIZACIÓN \_ DE MCI DGV \_ \_ FUERA
</dt> <dd>

El área fuera de la región especificada para la marca \_ MCI DGV \_ FREEZE AT está \_ inmovilizada.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpFreeze* apunta a una estructura [**MCI \_ DGV \_ FREEZE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms)

El tipo de dispositivo **vcr** usa las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>CAMPO \_ INMOVILIZAR VCR DE MCI \_ \_
</dt> <dd>

Inmovilizar solo un miembro del marco actual.

</dd> <dt>

<span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>FOTOGRAMA \_ INMOVILIZADO DE VCR de MCI \_ \_
</dt> <dd>

Inmovilizar ambos campos del marco actual.

</dd> <dt>

<span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>ENTRADA DE \_ INMOVILIZACIÓN DE VCR \_ DE MCI \_
</dt> <dd>

Inmovilizar el marco actual en la pantalla (se usa para la grabación).

</dd> <dt>

<span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>SALIDA DE \_ INMOVILIZACIÓN DE VCR DE MCI \_ \_
</dt> <dd>

Inmovilizar el fotograma actual del VCR (se usa con la captura de fotogramas).

</dd> </dl>

En el caso de los dispositivos *VCR, el parámetro lpFreeze* apunta a una estructura [**\_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md)

El tipo de dispositivo superpuesto usa la **siguiente marca** adicional:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpFreeze* contiene un rectángulo válido. Si no se especifica esta marca, el controlador del dispositivo inmovilizará todo el marco.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpFreeze* apunta a una estructura [**\_ \_ MCI OVLY RECT \_ PARMS.**](mci-ovly-rect-parms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

