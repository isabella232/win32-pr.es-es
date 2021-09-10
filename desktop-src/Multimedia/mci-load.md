---
title: MCI_LOAD comando (Mmsystem.h)
description: El comando LOAD de MCI \_ carga un archivo. Los dispositivos de superposición de vídeo digital y vídeo reconocen este comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370009"
---
# <a name="mci_load-command"></a>Comando LOAD de MCI \_

El comando LOAD de MCI \_ carga un archivo. Los dispositivos de superposición de vídeo digital y vídeo reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
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

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

Puntero a una [**estructura \_ MCI LOAD \_ PARMS.**](mci-load-parms.md) (Los dispositivos con parámetros adicionales pueden reemplazar esta estructura por una estructura específica del dispositivo. En el caso de los dispositivos de vídeo digital, el parámetro **lpLoad** apunta a una estructura [**\_ MCI DGV \_ LOAD \_ PARMS).**](/previous-versions//dd743391(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La siguiente marca adicional se aplica a todos los dispositivos que admiten MCI \_ LOAD:

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>ARCHIVO DE \_ CARGA \_ DE MCI
</dt> <dd>

El **miembro lpfilename** de la estructura identificada por *lpLoad* contiene una dirección de un búfer que contiene el nombre de archivo.

</dd> </dl>

La siguiente marca adicional se usa con el tipo **de dispositivo superpuesto:**

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpLoad* contiene un rectángulo de presentación válido que identifica el área del búfer de vídeo que se actualizará.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpLoad* apunta a una estructura [**MCI \_ OVLY \_ LOAD \_ PARMS.**](mci-ovly-load-parms.md)

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

 

