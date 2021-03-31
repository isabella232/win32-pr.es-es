---
title: Comando MCI_STEP (mmsystem. h)
description: El comando de paso de MCI \_ indica al reproductor uno o varios fotogramas. Los dispositivos de vídeo digital-video, VCR y CAV-Format reconocen este comando.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- Comando de MCI_STEP de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149876"
---
# <a name="mci_step-command"></a>Comando de paso de MCI \_

El comando de paso de MCI \_ indica al reproductor uno o varios fotogramas. Los dispositivos de vídeo digital-video, VCR y CAV-Format reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
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

<span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando admite dispositivos que devuelven **true** a \_ la \_ \_ marca de vídeo MCI GETDEVCAPS tiene el comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_marcos de \_ paso de DGV de MCI \_
</dt> <dd>

El miembro **dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas que se van a avanzar antes de mostrar otra imagen.

</dd> <dt>

<span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>paso de DGV de MCI \_ \_ \_ inverso
</dt> <dd>

Pasos en orden inverso.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpStep* apunta a una estructura [**parms de MCI \_ DGV \_ Step \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>fotogramas de VCR de MCI \_ \_ \_
</dt> <dd>

El miembro **dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas que se van a avanzar antes de mostrar otra imagen.

</dd> <dt>

<span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>desplazar VCR de MCI hacia \_ \_ \_ atrás
</dt> <dd>

Pasos en orden inverso.

</dd> </dl>

En el caso de los dispositivos VCR, el parámetro *lpStep* apunta a una estructura [**MCI \_ VCR \_ Step \_ parms**](mci-vcr-step-parms.md) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo de **videodisco** :

<dl> <dt>

<span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>marcos de paso de MCI \_ Vd \_ \_
</dt> <dd>

El miembro **dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas que se van a recorrer.

</dd> <dt>

<span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>paso de MCI \_ Vd \_ \_ inverso
</dt> <dd>

Pasos en orden inverso.

</dd> </dl>

En el caso de los dispositivos de videodisco, el parámetro *lpStep* apunta a una estructura [**parms de MCI \_ Vd \_ Step \_**](mci-vd-step-parms.md) .

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

 

