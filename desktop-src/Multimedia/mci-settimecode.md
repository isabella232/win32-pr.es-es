---
title: Comando MCI_SETTIMECODE (mmsystem. h)
description: El \_ comando MCI SETTIMECODE habilita o deshabilita la grabación de código de tiempo para un VCR. Los dispositivos VCR reconocen este comando.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- Comando de MCI_SETTIMECODE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676983"
---
# <a name="mci_settimecode-command"></a>\_Comando MCI SETTIMECODE

El \_ comando MCI SETTIMECODE habilita o deshabilita la grabación de código de tiempo para un VCR. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
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

<span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La marca adicional siguiente se aplica a los dispositivos VCR:

<dl> <dt>

<span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_registro de \_ SETTIMECODE de VCR de MCI \_
</dt> <dd>

Establece la grabación de seguimiento de código de tiempo en activado o desactivado. Esta marca se usa en combinación con una de las siguientes marcas adicionales:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_
</dt> <dd>

Grabación de código de tiempo activada.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_
</dt> <dd>

Grabación de código de tiempo desactivada.

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

 

