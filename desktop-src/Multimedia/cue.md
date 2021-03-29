---
title: comando de pila
description: El comando de pila se prepara para reproducir o grabar. Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- comando CUE Windows multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905663"
---
# <a name="cue-command"></a>comando de pila

El comando de pila se prepara para reproducir o grabar. Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

Marca que prepara un dispositivo para la reproducción o grabación. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando de **pila** y las marcas usadas por cada tipo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Pila</th>
<th>Pila</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td><ul>
<li>input</li>
<li>nomostrar</li>
</ul></td>
<td><ul>
<li>output</li>
<li>para <em>colocar</em></li>
</ul></td>
</tr>
<tr class="even">
<td>vídeos</td>
<td><ul>
<li>desde la <em>posición</em></li>
<li>input</li>
<li>output</li>
</ul></td>
<td><ul>
<li>preprocesará</li>
<li>reverse</li>
<li>para <em>colocar</em></li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td>input</td>
<td>output</td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszInOutTo* y su significado.



| Value           | Significado                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| desde la *posición* | Indica dónde comenzar.                                                                                                                                                                                                                                                                                      |
| input           | Se prepara para la grabación. En el caso de los dispositivos de vídeo digital, esta marca se puede omitir si el origen de presentación actual ya es la entrada externa.                                                                                                                                                                  |
| nomostrar          | Prepara para reproducir un marco sin mostrarlo. Cuando se especifica esta marca, la pantalla continúa mostrando la imagen en el búfer de fotogramas aunque su fotograma correspondiente no sea la posición actual. Un comando de pila subsiguiente sin esta marca y sin la marca "para" muestra el marco actual. |
| output          | Se prepara para la reproducción. Si no se especifica "Input" ni "Output", el valor predeterminado es "Output".                                                                                                                                                                                                           |
| preprocesará         | Mueve la distancia de predesplazamiento desde el *punto*. El en el punto es la posición actual o la posición especificada por el indicador "desde".                                                                                                                                                                            |
| reverse         | Indica que la dirección de reproducción está en orden inverso (hacia atrás).                                                                                                                                                                                                                                                             |
| para *colocar*   | Mueve el área de trabajo a la posición especificada. En el caso de los dispositivos VCR, esta marca indica dónde debe detenerse.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Aunque no es necesario, la emisión del comando de pila antes de reproducir o grabar en algunos dispositivos podría reducir el retraso antes de que el dispositivo inicie la acción.

Este comando produce un error si la reproducción o grabación está en curso o si el dispositivo está en pausa.

Cuando se cueing para la reproducción (mediante la indicación "Output"), la emisión del comando [Play](play.md) con la marca "from", "to" o "REVERSE" cancela el comando CUE.

Cuando se cueing para grabar (mediante la entrada "Input"), la emisión del comando [Record](record.md) con la marca "from", "to" o "Initialize" cancela el comando CUE.

## <a name="examples"></a>Ejemplos

El siguiente comando prepara el dispositivo "" de "" para grabar.

``` syntax
cue mysound input
```

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
</dt> <dt>

[reproducción](play.md)
</dt> <dt>

[record](record.md)
</dt> </dl>

 

