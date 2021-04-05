---
title: Comando MCI_FREEZE (mmsystem. h)
description: El \_ comando MCI Freeze inmoviliza el movimiento en la pantalla. Los dispositivos digitales-vídeo, superposición de vídeo y VCR reconocen este comando.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- Comando de MCI_FREEZE de Windows multimedia
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
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079066"
---
# <a name="mci_freeze-command"></a>\_Comando MCI Freeze

El \_ comando MCI Freeze inmoviliza el movimiento en la pantalla. Los dispositivos digitales-vídeo, superposición de vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con parámetros adicionales podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El tipo de dispositivo **DigitalVideo** usa las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_DGV \_ de MCI congelado \_ en
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpFreeze* contiene un rectángulo válido. El rectángulo especifica una región en el búfer de fotogramas que tendrá el bit de máscara de bloqueo para cada píxel activado. Los píxeles especificados no se actualizarán hasta que el bit de la máscara de bloqueo esté desactivado. Si no se especifica esta marca, el rectángulo tiene como valor predeterminado el búfer de fotogramas completo. Esta marca solo se admite si el comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) devuelve **true** para la \_ marca MCI DGV \_ GETDEVCAPS \_ Can \_ Lock.

</dd> <dt>

<span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>desbloqueo de DGV de MCI \_ \_ \_ fuera de
</dt> <dd>

El área fuera de la región especificada para la \_ marca MCI DGV \_ Freeze \_ at está inmovilizada.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpFreeze* apunta a una estructura de [**\_ DGV \_ Freeze \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .

El tipo de dispositivo **VCR** usa las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_campo MCI VCR \_ Freeze \_
</dt> <dd>

Inmoviliza solo un miembro del marco actual.

</dd> <dt>

<span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_marco de \_ desbloqueo de VCR de MCI \_
</dt> <dd>

Inmoviliza ambos campos del marco actual.

</dd> <dt>

<span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_entrada de \_ inmovilización de VCR de MCI \_
</dt> <dd>

Inmoviliza el marco actual en la pantalla (se usa para la grabación).

</dd> <dt>

<span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_salida de \_ desbloqueo de VCR de MCI \_
</dt> <dd>

Inmovilizar el fotograma actual del VCR (usado con la captura de fotogramas).

</dd> </dl>

En el caso de los dispositivos VCR, el parámetro *lpFreeze* apunta a una estructura [**\_ \_ parms genérica de MCI**](mci-generic-parms.md) .

El tipo de dispositivo **superpuesto** usa la siguiente marca adicional:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpFreeze* contiene un rectángulo válido. Si no se especifica esta marca, el controlador de dispositivo inmovilizará todo el marco.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpFreeze* apunta a una estructura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .

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

 

