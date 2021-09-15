---
title: MCI_CAPTURE comando (Mmsystem.h)
description: El comando MCI CAPTURE captura el contenido del búfer de \_ fotogramas y lo almacena en un archivo especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE comando Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476840"
---
# <a name="mci_capture-command"></a>Comando MCI \_ CAPTURE

El comando MCI CAPTURE captura el contenido del búfer de \_ fotogramas y lo almacena en un archivo especificado. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*
</dt> <dd>

Puntero a una [**estructura \_ MCI DGV \_ CAPTURE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>CAPTURA \_ DE MCI DGV \_ \_ COMO
</dt> <dd>

El **miembro lpstrFileName de** la estructura identificada por *lpCapture* contiene una dirección de un búfer que especifica la ruta de acceso de destino y el nombre de archivo. (Esta marca es obligatoria).

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI \_ DGV \_ CAPTURE \_ AT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpCapture* contiene un rectángulo válido. El rectángulo especifica la región rectangular dentro del búfer de marco que se recorta y se guarda en el disco. Si se omite, la región recortada tiene como valor predeterminado el rectángulo especificado o predeterminado en un comando PUT de [MCI \_ ](mci-put.md) anterior que especifica el área de origen para esta instancia del controlador de dispositivo.

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

 

