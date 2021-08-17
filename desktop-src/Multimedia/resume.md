---
title: comando resume
description: El comando resume continúa reproduciendo o grabando en un dispositivo que se ha pausado mediante el comando pause.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- comando resume Windows Multimedia
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e4a728e3ca89e2b4ddc21809830d5af3be9a2b04e004f99d5a792a9be5da01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801897"
---
# <a name="resume-command"></a>comando resume

El comando resume continúa reproduciendo o grabando en un dispositivo que se ha pausado mediante el [comando pause.](pause.md) Los dispositivos de vídeo digital, VCR y audio de onda reconocen este comando. Aunque los dispositivos cd audio, secuenciador MIDI y videodisc también reconocen este comando, los controladores de dispositivo MCICDA, MCISEQ y MCIPIONR no lo admiten.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
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

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="examples"></a>Ejemplos

El siguiente comando continúa reproduciendo o grabando el dispositivo "new sound".

``` syntax
resume newsound
```

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
</dt> <dt>

[pause](pause.md)
</dt> </dl>

 

