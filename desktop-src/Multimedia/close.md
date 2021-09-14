---
title: Comando close (Corecrt \_ io.h)
description: El comando close cierra el dispositivo o el archivo y los recursos asociados. MCI descarga un dispositivo cuando se cierran todas las instancias del dispositivo o todos los archivos. Todos los dispositivos MCI reconocen este comando.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- Comando close Windows Multimedia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069567"
---
# <a name="close-command"></a>Comando close

El comando close cierra el dispositivo o el archivo y los recursos asociados. MCI descarga un dispositivo cuando se cierran todas las instancias del dispositivo o todos los archivos. Todos los dispositivos MCI reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Para cerrar todos los dispositivos abiertos por la aplicación, especifique el identificador de dispositivo "all" para el *parámetro lpszDeviceID.*

Al cerrar el **dispositivo cdaudio,** se detiene la reproducción de audio.

**Windows 2000/XP:** Si se **reproduce el dispositivo cdaudio,** el cierre del **dispositivo cdaudio** no hace que el audio deje de reproducirse. Envíe primero [el comando](stop.md) stop.

## <a name="examples"></a>Ejemplos

El comando siguiente cierra el dispositivo "my sound".

``` syntax
close mysound
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Corecrt \_ io.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 

