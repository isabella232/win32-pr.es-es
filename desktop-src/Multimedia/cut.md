---
title: Comando cut
description: El comando cortar quita los datos del área de trabajo y los copia en el Portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- comando cut Windows Multimedia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369875"
---
# <a name="cut-command"></a>Comando cut

El comando cortar quita los datos del área de trabajo y los copia en el Portapapeles. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Una de las marcas siguientes identifica el elemento que se debe cortar.



| Value                 | Significado                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo*        | Especifica la parte de cada corte de marco. Si se omite, el valor predeterminado es todo el marco. Cuando se especifica este elemento, no se eliminan los marcos. En su lugar, el área dentro del rectángulo se vuelve negra.                                       |
| secuencia *de* audio | Especifica la secuencia de audio en el área de trabajo afectada por el comando . Si usa esta marca y también quiere cortar vídeo, también debe usar la marca "secuencia de vídeo". (Si no se especifica ninguna marca, se cortan todas las secuencias de audio y vídeo). |
| desde *la posición*       | Especifica el inicio del corte de intervalo. Si se omite, el valor predeterminado es la posición actual.                                                                                                                                                |
| para *colocar*         | Especifica el final del corte de intervalo. El corte de datos de audio y vídeo es exclusivo de esta posición. Si se omite, el valor predeterminado es el final del área de trabajo.                                                                                  |
| secuencia de *vídeo* | Especifica la secuencia de vídeo en el área de trabajo afectada por el comando . Si usa esta marca y también desea cortar audio, también debe usar la marca "secuencia de audio". (Si no se especifica ninguna marca, se cortan todas las secuencias de audio y vídeo). |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

El cambio se convierte en permanente solo cuando los datos se guardan explícitamente; sin embargo, la reproducción actúa como si se hubieran quitado los datos.

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

 

