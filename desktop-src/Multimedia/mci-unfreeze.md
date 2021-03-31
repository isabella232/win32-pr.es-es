---
title: Comando MCI_UNFREEZE (mmsystem. h)
description: El \_ comando MCI unfreeze restaura el movimiento en un área del búfer de vídeo inmovilizado con el \_ comando MCI Freeze. Los dispositivos digitales-vídeo, VCR y superposición de vídeo reconocen este comando.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- Comando de MCI_UNFREEZE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151030"
---
# <a name="mci_unfreeze-command"></a>\_Comando MCI UNfreeze

El \_ comando MCI unfreeze restaura el movimiento en un área del búfer de vídeo inmovilizado con el comando [MCI \_ Freeze](mci-freeze.md) . Los dispositivos digitales-vídeo, VCR y superposición de vídeo reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Con el tipo de dispositivo **DigitalVideo** se usa la siguiente marca adicional:

\_DGV \_ Rect

El miembro **RC** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido. El rectángulo especifica una región en el búfer de fotogramas cuyos píxeles deben tener el bit de máscara de bloqueo desactivado. Las regiones rectangulares se especifican como se describe en el comando [MCI \_ Put](mci-put.md) . Si se omite, el rectángulo tiene como valor predeterminado el búfer de fotogramas completo. Mediante el uso de una secuencia de comandos Freeze y unfreeze con distintos rectángulos, se pueden describir patrones arbitrarios de bits de máscara de bloqueos.

En el caso de los dispositivos de vídeo digital, el parámetro *lpUnfreeze* apunta a una estructura **\_ DGV \_ unfreeze \_ parms de MCI** . Para obtener más información, vea los comentarios de la estructura [**MCI \_ DGV \_ Rect \_ parms**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>\_entrada de \_ desbloqueo de VCR de MCI \_
</dt> <dd>

Libere la entrada.

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_salida de \_ desbloqueo de VCR de MCI \_
</dt> <dd>

Libere la salida.

</dd> </dl>

La siguiente marca adicional se usa con el tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido. Es un parámetro obligatorio.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpUnfreeze* apunta a una estructura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .

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

 

