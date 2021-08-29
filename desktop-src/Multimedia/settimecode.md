---
title: Comando settimecode
description: El comando settimecode habilita o deshabilita la grabación de código de tiempo para un VCR. Los dispositivos VCR reconocen este comando.
ms.assetid: 1b4b82e8-4f13-4bc9-afb0-796339cabb51
keywords:
- Comando settimecode Windows Multimedia
topic_type:
- apiref
api_name:
- settimecode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19c6516586e1f8f3972193ef5723fb0843635fd2e28dda9dbecc5ce13ef8414b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037275"
---
# <a name="settimecode-command"></a>Comando settimecode

El comando settimecode habilita o deshabilita la grabación de código de tiempo para un VCR. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settimecode %s %s %s"), 
  lpszDeviceID,
  lpszTimecode, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*
</dt> <dd>

Una de las marcas siguientes.



| Value      | Significado                          |
|------------|----------------------------------|
| registro en  | Establece vcr para registrar el código de tiempo. |
| record off | Deshabilita la grabación de código de tiempo.     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 

