---
description: Muestra cómo usar el procesamiento de vídeo de DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Ejemplo de DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360098"
---
# <a name="dxva2_videoproc-sample"></a>DXVA2 \_ ejemplo de Videoproc

Muestra cómo usar el [procesamiento de vídeo de DXVA](dxva-video-processing.md).

Este ejemplo genera mediante programación un vídeo con un flujo principal y un subflujo. El flujo principal muestra las barras de color SMPTE y el subflujo es un rectángulo semitransparente. A continuación, el vídeo se procesa y se muestra mediante un procesador de vídeo DXVA. El usuario puede cambiar los valores alfa planos, los rectángulos de origen y de destino, los ajustes de color y el espacio de colores.

![captura de pantalla del \- ejemplo de videoproc de dxva2](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>API mostradas

En este ejemplo se muestran las siguientes interfaces de DXVA:

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Uso

El \_ ejemplo de Videoproc DXVA2 crea una aplicación de Windows.

Opciones de la línea de comandos:



| Opción | Descripción                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -HH    | Fuerza a la aplicación a usar un dispositivo Direct3D de hardware y un dispositivo DXVA de hardware. |
| -HS    | Fuerza a la aplicación a usar un dispositivo Direct3D de hardware y un dispositivo de software DXVA. |
| -ss    | Fuerza a la aplicación a usar un dispositivo Direct3D de software y un dispositivo de software DXVA. |



 

Comandos de teclado:



| Clave       | Descripción                                             |
|-----------|---------------------------------------------------------|
| ALT+ENTRAR | Cambiar entre el modo de ventana y el modo de pantalla completa.      |
| F1: F8     | Escriba uno de los modos que se muestran en la tabla siguiente.    |
| FIN       | Habilitar o deshabilitar el registro de depuración para fotogramas quitados. |
| INICIO      | Restablezca un parámetro a su valor inicial.                 |



 

Cada una de las teclas de función F1 a F8 cambia a un modo en el que se pueden utilizar las teclas de dirección para ajustar un parámetro de representación determinado. Además, cambia el color de la subsecuencia.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Clave</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>F1</td>
<td>Ajuste los valores alfa.<br/>
<ul>
<li>SUBIR: aumente el alfa plano de ambos flujos.</li>
<li>DOWN: reduce el alfa plano de ambos flujos.</li>
<li>RIGHT: aumentar el alfa de píxeles de la subsecuencia.</li>
<li>LEFT: reduce el píxel alfa de la subsecuencia.</li>
</ul>
Color de subsecuencia: blanco<br/></td>
</tr>
<tr class="even">
<td>F2</td>
<td>Ajuste el área de origen (zoom) del flujo principal.<br/>
<ul>
<li>SUBIR: aumentar verticalmente (acercar).</li>
<li>ABAJO: reducir verticalmente (alejar).</li>
<li>RIGHT: aumentar horizontalmente (acercar).</li>
<li>LEFT: disminuir horizontalmente (alejar).</li>
</ul>
Color de subsecuencia: rojo<br/></td>
</tr>
<tr class="odd">
<td>F3</td>
<td>Mueva el área de origen del flujo principal.<br/>
<ul>
<li>SUBIR: subir.</li>
<li>ABAJO: bajar.</li>
<li>DERECHA: moverse a la derecha.</li>
<li>IZQUIERDA: moverse a la izquierda.</li>
</ul>
Color de subsecuencia: amarillo<br/></td>
</tr>
<tr class="even">
<td>F4</td>
<td>Ajuste el área de destino del flujo principal.<br/>
<ul>
<li>SUBIR: aumentar verticalmente.</li>
<li>ABAJO: reducir verticalmente.</li>
<li>RIGHT: aumentar horizontalmente.</li>
<li>LEFT: disminuir horizontalmente.</li>
</ul>
Color de subsecuencia: verde<br/></td>
</tr>
<tr class="odd">
<td>F5</td>
<td>Mueva el área de destino del flujo principal.<br/>
<ul>
<li>SUBIR: subir.</li>
<li>ABAJO: bajar.</li>
<li>DERECHA: moverse a la derecha.</li>
<li>IZQUIERDA: moverse a la izquierda.</li>
</ul>
Color de subsecuencia: Aguamarina<br/></td>
</tr>
<tr class="even">
<td>F6</td>
<td>Cambiar el color de fondo o el espacio de colores.<br/>
<ul>
<li>Subir, bajar: desplazarse por los espacios de colores.</li>
<li>DERECHA, izquierda: desplazarse por los colores de fondo.</li>
</ul>
Color de subsecuencia: azul<br/></td>
</tr>
<tr class="odd">
<td>F7</td>
<td>Ajustar el brillo y el contraste.<br/>
<ul>
<li>SUBIR: aumentar el brillo.</li>
<li>ABAJO: reduce el brillo.</li>
<li>RIGHT: aumentar contraste.</li>
<li>LEFT: reduce el contraste.</li>
</ul>
Color de subsecuencia: magenta<br/></td>
</tr>
<tr class="even">
<td>F8</td>
<td>Ajuste el matiz y la saturación.<br/>
<ul>
<li>SUBIR: aumentar matiz.</li>
<li>BAJAR: reduce el matiz.</li>
<li>RIGHT: aumentar la saturación.</li>
<li>LEFT: disminución de la saturación.</li>
</ul>
Color de subsecuencia: negro<br/></td>
</tr>
</tbody>
</table>



 

En cada modo, al presionar la tecla Inicio, se restablecen los parámetros de ese modo a sus valores iniciales.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Procesamiento de vídeo de DXVA](dxva-video-processing.md)
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




