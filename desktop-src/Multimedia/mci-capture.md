---
title: Comando MCI_CAPTURE (mmsystem. h)
description: El \_ comando MCI Capture captura el contenido del búfer de fotogramas y lo almacena en un archivo especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- Comando de MCI_CAPTURE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996703"
---
# <a name="mci_capture-command"></a>\_Comando MCI Capture

El \_ comando MCI Capture captura el contenido del búfer de fotogramas y lo almacena en un archivo especificado. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
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

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*
</dt> <dd>

Puntero a una estructura de [**\_ \_ \_ parms de captura DGV de MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>\_ \_ captura de DGV MCI \_ como
</dt> <dd>

El miembro **lpstrFileName** de la estructura identificada por *lpCapture* contiene una dirección de un búfer que especifica la ruta de acceso y el nombre de archivo de destino. (Esta marca es obligatoria).

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_ \_ captura de DGV \_ de MCI en
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpCapture* contiene un rectángulo válido. El rectángulo especifica la región rectangular dentro del búfer de fotogramas que se recorta y se guarda en el disco. Si se omite, el valor predeterminado de la región recortado es el rectángulo especificado o predeterminado en un comando anterior de [MCI \_ Put](mci-put.md) que especifica el área de origen para esta instancia del controlador de dispositivo.

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

 

