---
title: comando freeze
description: El comando freeze inmoviliza la entrada de vídeo o la salida de vídeo en un VCR o deshabilita la adquisición de vídeo en el búfer de fotogramas. Los dispositivos de vídeo digital, superposición de vídeo y VCR reconocen este comando.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- comando freeze Windows Multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1261cc75575a5b59d200ff965a5325caef9fa966
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481561"
---
# <a name="freeze-command"></a>comando freeze

El comando freeze inmoviliza la entrada de vídeo o la salida de vídeo en un VCR o deshabilita la adquisición de vídeo en el búfer de fotogramas. Los dispositivos de vídeo digital, superposición de vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*
</dt> <dd>

Marca que identifica qué se debe inmovilizar. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **freeze** y las marcas usadas por cada tipo.




| Valor | Significado | Significado | 
|-------|---------|---------|
| digitalvideo | en <em>rectángulo</em> | Fuera | 
| overlay | en <em>rectángulo</em> | 
| Vcr | <ul><li>campo</li><li>frame</li></ul> | <ul><li>input</li><li>output</li></ul> | 




 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszFreezeFlags* y sus significados.



| Valor          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo* | Especifica la región que se inmovilizará. En el caso de los dispositivos de superposición de vídeo, esta región tendrá deshabilitada la adquisición de vídeo. En el caso de los dispositivos de vídeo digital, los píxeles dentro del rectángulo tendrán el bit de máscara de bloqueo activado (a menos que se especifique la marca "fuera"). El rectángulo es relativo al origen del búfer de vídeo y se especifica como *X1 Y1 X2 Y2*. Las coordenadas *X1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *X2 Y2* especifican el ancho y el alto. |
| campo          | Inmoviliza el primer campo. El campo se asume de forma predeterminada (si no se especifica ningún marco ni campo).                                                                                                                                                                                                                                                                                                                                                                                               |
| frame          | Inmoviliza todo el marco y muestra ambos campos.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| input          | Inmoviliza el marco actual de la imagen de entrada, ya sea en pausa o en ejecución.                                                                                                                                                                                                                                                                                                                                                                                                                |
| output         | Inmoviliza el marco actual de la salida del VCR. Si el VCR se reproduce cuando se emite inmovilización, el marco actual se inmoviliza y el VCR se pausa. Si el VCR se pausa cuando se emite este comando, se inmoviliza el marco actual. La imagen inmovilizada permanece en el dispositivo de salida hasta que [se emite](unfreeze.md) un comando de descongelar. Si no se especifica "input" ni "output", se asume "output".                                                                                    |
| Fuera        | Indica que el área fuera de la región especificada mediante la marca "at" está inmovilizada.                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Cuando se usa con dispositivos VCR, este comando está pensado para tarjetas de captura de fotogramas.

Para especificar regiones de adquisición irregulares con la marca "at", use una serie de comandos freeze y [unfreeze.](unfreeze.md) Algunos dispositivos de superposición de vídeo limitan la complejidad de la región de adquisición.

Este comando solo se admite si una llamada al comando [de](capability.md) funcionalidad con la marca "can freeze" devuelve **TRUE.**

## <a name="examples"></a>Ejemplos

El comando siguiente deshabilita la adquisición de vídeo en un cuadrado de 100 píxeles en la esquina superior izquierda del búfer de vídeo.

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[capability](capability.md)
</dt> <dt>

[Descongelar](unfreeze.md)
</dt> </dl>

 

