---
description: Combinación de captura de vídeo y versión preliminar
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinación de captura de vídeo y versión preliminar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1894e9431cbfa9e7bbbd0ef0bcec48021055350030b54ffd2f3e2729db81c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084335"
---
# <a name="combining-video-capture-and-preview"></a>Combinación de captura de vídeo y versión preliminar

En las secciones anteriores se describe cómo capturar vídeo en varios formatos de archivo. En la sección [Vista previa de vídeo](previewing-video.md) se describe cómo crear un gráfico de vista previa en directo. Sin embargo, muchas aplicaciones deben hacer ambas a la vez. Para crear una vista previa combinada y un gráfico de escritura de archivos, basta con realizar dos llamadas a [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



En este código, capture Graph Builder oculta algunos detalles:

-   Si el filtro de captura tiene un pin de vista previa o un pin de puerto de vídeo, además de un pin de captura, el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) simplemente representa ambos pines, como se muestra en la ilustración siguiente.

    ![gráfico de captura y vista previa](images/vidcap04.png)

-   Si el filtro solo tiene un pin de captura, Capture Graph Builder usa el [filtro Smart Tee](smart-tee-filter.md) para dividir la secuencia de captura. En la ilustración siguiente se muestra el gráfico con una tee inteligente.

    ![Captura y vista previa del gráfico con filtro de tee inteligente](images/vidcap05.png)

El filtro Smart Tee tiene un pin de captura y un pin de vista previa. Toma una única secuencia de vídeo del filtro de captura y la divide en dos secuencias, una para la captura y otra para la versión preliminar. Para mantener el rendimiento en el pin de captura, el pin de vista previa quita los fotogramas según sea necesario. También quita las marcas de tiempo de cada ejemplo antes de entregarla, por los motivos que se deban en el tema [DirectShow filtros de captura de vídeo](directshow-video-capture-filters.md).

Aunque smart tee divide la secuencia, no duplica físicamente los datos de vídeo. En su lugar, usa objetos de ejemplo multimedia personalizados que comparten los búferes. Los ejemplos se marcan como de "solo lectura" para asegurarse de que los filtros de nivel inferior no escriben en los datos.

Si el gráfico de captura tiene una ventana de vista previa, varias cosas pueden hacer que el Administrador de filtros Graph detenga todo el gráfico, incluida la secuencia de captura:

-   Bloquear el equipo.
-   Presione CTRL+ALT+SUPR en un equipo que sea miembro de un dominio.
-   Ejecutar una aplicación direct3D de pantalla completa, como un juego o un protector de pantalla.
-   Cambiar monitores o cambiar la resolución de pantalla.
-   Ejecutar un programa que hace que Windows un cuadro de diálogo Control de cuentas de usuario (UAC). (Windows Vista o posterior).
-   Ejecución de una ventana DOS de pantalla completa.

Cualquiera de estos eventos podría interrumpir la sesión de captura, lo que posiblemente provocaría la pérdida de datos. (Esto es lo que sucede internamente: el representador de vídeo pierde los recursos de Direct3D o DirectDraw que necesita. En el proceso de recuperación de esos recursos, el representador de vídeo debe volver a conectarse con el filtro ascendente, lo que hace que filter Graph Manager detenga el gráfico).

A continuación se ofrecen dos soluciones posibles a este problema:

-   No incluya una secuencia de versión preliminar. Sin embargo, tenga en cuenta que el método [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) agrega automáticamente una ventana de vista previa cuando el dispositivo de captura tiene un pin de puerto de vídeo. Vea [Video Port Pins in File Capture (Anclar puertos de vídeo en la captura de archivos).](video-port-pins-in-file-capture.md)
-   Use el motor de búfer de flujo para enviar la secuencia de vista previa a un gráfico en otro proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



