---
description: Muestra cómo usar el procesamiento de vídeo DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc4be1bad6a3955af255cb083a4595ecedfd30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252494"
---
# <a name="dxva2_videoproc-sample"></a>Ejemplo de VideoProc de DXVA2 \_

Muestra cómo usar el procesamiento [de vídeo DXVA.](dxva-video-processing.md)

Este ejemplo genera vídeo mediante programación con una secuencia principal y una subsección. La secuencia principal muestra las barras de color SMPTE y la subsección es un rectángulo semitransparente. A continuación, el vídeo se procesa y se muestra mediante un procesador de vídeo DXVA. El usuario puede cambiar los valores alfa planas, los rectángulos de origen y destino, los ajustes de color y el espacio de color.

![captura de pantalla del ejemplo de \- videoproc dxva2](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las siguientes interfaces DXVA:

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Uso

El ejemplo DXVA2 \_ VideoProc crea una Windows aplicación.

Opciones de línea de comandos:



| Opción | Descripción                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | Obliga a la aplicación a usar un dispositivo Direct3D de hardware y un dispositivo DXVA de hardware. |
| -hs    | Obliga a la aplicación a usar un dispositivo Direct3D de hardware y un dispositivo DXVA de software. |
| -ss    | Obliga a la aplicación a usar un dispositivo Direct3D de software y un dispositivo DXVA de software. |



 

Comandos de teclado:



| Clave       | Descripción                                             |
|-----------|---------------------------------------------------------|
| ALT+ENTRAR | Cambie entre el modo de ventana y el modo de pantalla completa.      |
| F1–F8     | Escriba uno de los modos que se muestran en la tabla siguiente.    |
| FIN       | Habilite o deshabilite el registro de depuración para fotogramas eliminados. |
| INICIO      | Restablezca un parámetro a su valor inicial.                 |



 

Cada una de las teclas de función de F1 a F8 cambia a un modo en el que las teclas de dirección se pueden usar para ajustar un parámetro de representación determinado. Además, cambia el color de la secuencia inferior.




| Clave | Descripción | 
|-----|-------------|
| F1 | Ajuste los valores alfa.<br /><ul><li>UP: aumente el alfa planar de ambas secuencias.</li><li>DOWN: reduzca el alfa planar de ambas secuencias.</li><li>RIGHT: aumente el píxel alfa de la subsección.</li><li>LEFT: reduzca el píxel alfa de la subsección.</li></ul>Color de substream: Blanco<br /> | 
| F2 | Ajuste el área de origen del flujo principal (zoom).<br /><ul><li>SUBIR: aumente verticalmente (acercar).</li><li>DOWN: disminuir verticalmente (alejar).</li><li>RIGHT: Aumentar horizontalmente (acercar).</li><li>LEFT: reducir horizontalmente (alejar).</li></ul>Color de subtransmisión: rojo<br /> | 
| F3 | Mueva el área de origen del flujo principal.<br /><ul><li>SUBIR: subir.</li><li>DOWN: bajar.</li><li>RIGHT: moverse a la derecha.</li><li>LEFT: mover a la izquierda.</li></ul>Color de subtransmisión: amarillo<br /> | 
| F4 | Ajuste el área de destino del flujo principal.<br /><ul><li>UP: aumente verticalmente.</li><li>DOWN: disminuir verticalmente.</li><li>RIGHT: aumente horizontalmente.</li><li>LEFT: disminuir horizontalmente.</li></ul>Color de substream: Verde<br /> | 
| F5 | Mueva el área de destino del flujo principal.<br /><ul><li>SUBIR: subir.</li><li>DOWN: bajar.</li><li>RIGHT: moverse a la derecha.</li><li>LEFT: mover a la izquierda.</li></ul>Color de subtransmisión: Cian<br /> | 
| F6 | Cambiar el color de fondo o el espacio de color.<br /><ul><li>UP, DOWN: recorrer los espacios de color.</li><li>RIGHT, LEFT: recorrer los colores de fondo.</li></ul>Color de substream: Azul<br /> | 
| F7 | Ajuste el brillo y el contraste.<br /><ul><li>UP: aumente el brillo.</li><li>DOWN: disminuir el brillo.</li><li>RIGHT: aumente el contraste.</li><li>LEFT: disminuir el contraste.</li></ul>Color de substream: Magenta<br /> | 
| F8 | Ajuste el matiz y la saturación.<br /><ul><li>UP: aumente el matiz.</li><li>DOWN: disminuir el matiz.</li><li>RIGHT: Aumente la saturación.</li><li>LEFT: disminuir la saturación.</li></ul>Color de subtransmisión: negro<br /> | 




 

En cada modo, al presionar la tecla HOME se restablecen los parámetros de ese modo a sus valores iniciales.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de github Windows ejemplos clásicos](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Procesamiento de vídeo DXVA](dxva-video-processing.md)
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




