---
title: MCI_MARK comando (Mmsystem.h)
description: El comando MCI MARK registra o borra marcas que se pueden usar con el comando MCI SEEK para \_ \_ búsquedas de alta velocidad. Los dispositivos VCR reconocen este comando.
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
ms.openlocfilehash: e83cdb6c8c62fa19d66dc6042b6c8b16837f9dc4657060c0955098ed90e1c016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375000"
---
# <a name="mci_mark-command"></a>Comando MCI \_ MARK

El comando MCI MARK registra o borra marcas que se pueden usar con el comando \_ [ \_ MCI SEEK](mci-seek.md) para búsquedas de alta velocidad. Los dispositivos VCR reconocen este comando.

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

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 

