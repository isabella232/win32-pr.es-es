---
title: Freeze (comando)
description: El comando Freeze inmoviliza la entrada de vídeo o la salida de vídeo en un VCR o deshabilita la adquisición de vídeo en el búfer de fotogramas. Los dispositivos digitales-vídeo, superposición de vídeo y VCR reconocen este comando.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- comando Freeze Windows multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078844"
---
# <a name="freeze-command"></a>Freeze (comando)

El comando Freeze inmoviliza la entrada de vídeo o la salida de vídeo en un VCR o deshabilita la adquisición de vídeo en el búfer de fotogramas. Los dispositivos digitales-vídeo, superposición de vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca que identifica lo que se va a inmovilizar. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Freeze** y las marcas usadas por cada tipo.



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
<td>en el <em>rectángulo</em></td>
<td>ajena</td>
</tr>
<tr class="even">
<td>overlay</td>
<td>en el <em>rectángulo</em></td>

</tr>
<tr class="odd">
<td>vídeos</td>
<td><ul>
<li>campo</li>
<li>frame</li>
</ul></td>
<td><ul>
<li>input</li>
<li>output</li>
</ul></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszFreezeFlags* y su significado.



| Value          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en el *rectángulo* | Especifica la región que se va a inmovilizar. En el caso de los dispositivos de superposición de vídeo, esta región tendrá deshabilitada la adquisición de vídeo. En el caso de los dispositivos de vídeo digital, los píxeles del rectángulo tendrán el bit de máscara de bloqueo activado (a menos que se especifique la marca "exterior"). El rectángulo es relativo al origen del búfer de vídeo y se especifica como *x1 Y1 x2 Y2*. Las coordenadas *x1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *x2 Y2* especifican el ancho y el alto. |
| campo          | Inmoviliza el primer campo. El campo se supone de forma predeterminada (si no se especifica ningún marco ni campo).                                                                                                                                                                                                                                                                                                                                                                                               |
| frame          | Inmoviliza todo el marco, mostrando ambos campos.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| input          | Inmoviliza el marco actual de la imagen de entrada, si está en pausa o en ejecución.                                                                                                                                                                                                                                                                                                                                                                                                                |
| output         | Inmoviliza el marco actual de la salida del VCR. Si el VCR se está reproduciendo cuando se emite la inmovilización, el fotograma actual se congela y el VCR está en pausa. Si el VCR está en pausa cuando se emite este comando, se inmoviliza el marco actual. La imagen inmovilizada permanece en el dispositivo de salida hasta que se emite un comando [unfreeze](unfreeze.md) . Si no se especifica "Input" ni "Output", se asume "Output".                                                                                    |
| ajena        | Indica que el área fuera de la región especificada mediante la marca "at" está inmovilizada.                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se usa con dispositivos VCR, este comando está pensado para tarjetas que capturan fotogramas.

Para especificar regiones de adquisición irregulares con la marca "at", use una serie de comandos Freeze y [unfreeze](unfreeze.md) . Algunos dispositivos de superposición de vídeo limitan la complejidad de la región de adquisición.

Este comando solo se admite si una llamada al comando [Capability](capability.md) con la marca "puede inmovilizar" devuelve **true**.

## <a name="examples"></a>Ejemplos

El siguiente comando deshabilita la adquisición de vídeo en un cuadrado de 100 píxeles en la esquina superior izquierda del búfer de vídeo.

``` syntax
freeze vboard at 0 0 100 100
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

[capability](capability.md)
</dt> <dt>

[liberar](unfreeze.md)
</dt> </dl>

 

