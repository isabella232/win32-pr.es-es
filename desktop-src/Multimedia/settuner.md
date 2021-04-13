---
title: comando settuner
description: El comando settuner cambia el sintonizador actual o la configuración de canal del sintonizador actual. Los dispositivos VCR reconocen este comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- comando settuner de Windows multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493259"
---
# <a name="settuner-command"></a>comando settuner

El comando settuner cambia el sintonizador actual o la configuración de canal del sintonizador actual. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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
| *canal* de canal                | Establece el sintonizador en el *canal*. Es posible que no pueda cambiar el canal durante la grabación, según el VCR. Un canal mayor que el máximo establece el sintonizador en el canal máximo.                                                                                                                    |
| búsqueda de canal activo de búsqueda de canal | Busca el siguiente canal con una señal válida. "Buscar" incrementa el número de canal en su búsqueda. "Buscar hacia abajo" disminuye el número de canal en su búsqueda. El sintonizador se ajusta al canal 1 cuando se supera el número de canal máximo. Del mismo modo, al buscar hacia abajo, el sintonizador se ajusta al canal máximo. |
| canal inferior del canal           | Incrementa o disminuye el canal del sintonizador. Es posible que no pueda cambiar el canal durante la grabación, según el VCR. El sintonizador se ajusta al canal 1 cuando se supera el número de canal máximo. Del mismo modo, al buscar hacia abajo, el sintonizador se ajusta al canal máximo.                              |
| *número* de número                  | Especifica el sintonizador que debe verse afectado por el comando settuner. Si no se proporciona el *número* , se asume el valor predeterminado de 1.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify", "Test" o una combinación de estos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> </dl>

 

