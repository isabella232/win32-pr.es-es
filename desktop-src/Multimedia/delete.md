---
title: eliminar comando
description: El comando DELETE elimina un segmento de datos de un archivo. Los dispositivos de audio digital y de onda-vídeo reconocen este comando.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- comando DELETE de Windows multimedia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905573"
---
# <a name="delete-command"></a>eliminar comando

El comando DELETE elimina un segmento de datos de un archivo. Los dispositivos de audio digital y de onda-vídeo reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*
</dt> <dd>

Marca que identifica un segmento de datos que se va a eliminar. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Delete** y las marcas usadas por cada tipo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td><ul>
<li>en el <em>rectángulo</em></li>
<li><em>secuencia</em> de flujo de audio</li>
<li>desde la <em>posición</em></li>
</ul></td>
<td><ul>
<li>para <em>colocar</em></li>
<li><em>secuencia</em> de flujo de vídeo</li>
</ul></td>
</tr>
<tr class="even">
<td>waveaudio</td>
<td>desde la <em>posición</em></td>
<td>para <em>colocar</em></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszPosition* y su significado.



| Value                 | Significado                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en el *rectángulo*        | Especifica la parte de cada fotograma eliminada. Si se omite, el valor predeterminado es todo el marco. Cuando se especifica este elemento, no se eliminan los marcos. En su lugar, el área dentro del rectángulo se vuelve negra.                                          |
| *secuencia* de flujo de audio | Especifica la secuencia de audio en el área de trabajo afectada por el comando. Si usa esta marca y también desea eliminar vídeo, también debe usar la marca de "secuencia de vídeo". (Si no se especifica ninguna marca, se eliminan todas las secuencias de audio y vídeo). |
| desde la *posición*       | Especifica la posición en la que comienza la eliminación. Si se omite esta marca, la eliminación comienza en la posición actual.                                                                                                                       |
| para *colocar*         | Especifica la posición en la que finaliza la eliminación. Si se omite esta marca, la eliminación continúa hasta el final del contenido o del área de trabajo.                                                                                                       |
| *secuencia* de flujo de vídeo | Especifica la secuencia de vídeo en el área de trabajo afectada por el comando. Si usa esta marca y también desea eliminar audio, también debe usar la marca de "secuencia de audio". (Si no se especifica ninguna marca, se eliminan todas las secuencias de audio y vídeo).     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) .

## <a name="examples"></a>Ejemplos

El siguiente comando elimina los datos de audio de forma de onda de 1 milisegundo a 900 milisegundos (suponiendo que el formato de hora se establece en milisegundos).

``` syntax
delete mysound from 1 to 900
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

[set](set.md)
</dt> </dl>

 

