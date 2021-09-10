---
title: MCI_MARK comando (Mmsystem.h)
description: El comando MCI MARK registra o borra las marcas que se pueden usar con el comando MCI SEEK para \_ \_ búsquedas de alta velocidad. Los dispositivos VCR reconocen este comando.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- MCI_MARK comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370039"
---
# <a name="mci_mark-command"></a>Comando MCI \_ MARK

El comando MCI MARK registra o borra las marcas que se pueden usar con el comando \_ [ \_ MCI SEEK](mci-seek.md) para búsquedas de alta velocidad. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
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

<span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos VCR:

<dl> <dt>

<span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>BORRADO DE \_ MARCA DE VCR \_ DE MCI \_
</dt> <dd>

Borra una marca en la posición actual si existe una.

</dd> <dt>

<span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>ESCRITURA DE \_ MARCA DE VCR \_ DE MCI \_
</dt> <dd>

Escribe una marca en la posición actual.

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

 

