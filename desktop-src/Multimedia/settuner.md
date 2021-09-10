---
title: Comando settuner
description: El comando settuner cambia el ajuste actual o la configuración del canal del ajuste actual. Los dispositivos VCR reconocen este comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- Comando settuner Windows Multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370256"
---
# <a name="settuner-command"></a>Comando settuner

El comando settuner cambia el ajuste actual o la configuración del canal del ajuste actual. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*
</dt> <dd>

Una de las marcas siguientes.



| Value                            | Significado                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| canal *de canal*                | Establece el afinador en *el canal*. Es posible que no pueda cambiar el canal durante la grabación, en función del VCR. Un canal mayor que el máximo establece el afinador en el canal máximo.                                                                                                                    |
| channel seek upchannel seek down | Busca el canal siguiente con una señal válida. "Buscar" incrementa el número de canal en su búsqueda. "Buscar abajo" disminuye el número de canal en su búsqueda. El ajuste se ajusta al canal 1 cuando se supera el número máximo de canales. De forma similar, al buscar hacia abajo, el ajuste se ajusta al canal máximo. |
| canal hacia arriba y abajo           | Incrementa o disminuye el canal del tuner. Es posible que no pueda cambiar el canal durante la grabación, en función del VCR. El ajuste se ajusta al canal 1 cuando se supera el número máximo de canales. De forma similar, al buscar hacia abajo, el ajuste se ajusta al canal máximo.                              |
| number *number*                  | Especifica el ajuste que se va a ver afectado por el comando settuner. Si *no* se da number, se supone el valor predeterminado de 1.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 

