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
ms.openlocfilehash: 7075de6ed50c49773a502ba77e093d84e85b079a6b17c462ea8ee65ad1330aa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688805"
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



| Valor                            | Significado                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| canal *de canal*                | Establece el afinador en *el canal*. Es posible que no pueda cambiar el canal durante la grabación, dependiendo del VCR. Un canal mayor que el máximo establece el afinador en el canal máximo.                                                                                                                    |
| channel seek upchannel seek down | Busca el canal siguiente con una señal válida. "Buscar" incrementa el número de canal en su búsqueda. "Buscar abajo" disminuye el número de canal en su búsqueda. El ajuste se ajusta al canal 1 cuando se supera el número de canal máximo. De forma similar, al buscar hacia abajo, el ajuste se ajusta al canal máximo. |
| canal hacia arriba y abajo           | Incrementa o disminuye el canal del tuner. Es posible que no pueda cambiar el canal durante la grabación, dependiendo del VCR. El ajuste se ajusta al canal 1 cuando se supera el número de canal máximo. De forma similar, al buscar hacia abajo, el ajuste se ajusta al canal máximo.                              |
| number *number*                  | Especifica el ajuste que se va a ver afectado por el comando settuner. Si *no* se da number, se supone el valor predeterminado de 1.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 

