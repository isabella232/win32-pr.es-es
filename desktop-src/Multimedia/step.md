---
title: comando Step
description: El comando Step le indica cómo reproducir una o más tramas hacia delante o hacia atrás. La acción predeterminada es avanzar un fotograma. Los dispositivos de vídeo digital-video, VCR y CAV-Format reconocen este comando.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- comando Step multimedia de Windows
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490475"
---
# <a name="step-command"></a>comando Step

El comando Step le indica cómo reproducir una o más tramas hacia delante o hacia atrás. La acción predeterminada es avanzar un fotograma. Los dispositivos de vídeo digital-video, VCR y CAV-Format reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*
</dt> <dd>

Una o ambas de las marcas siguientes.



| Value       | Significado                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| por *fotogramas* | Indica el número de fotogramas que se van a recorrer. Si especifica un valor de *fotogramas* negativos, no puede especificar la marca "REVERSE". |
| reverse     | Desplazar los fotogramas en orden inverso.                                                                                              |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

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

 

