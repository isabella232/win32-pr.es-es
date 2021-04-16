---
description: Combinación de captura de vídeo y vista previa
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinación de captura de vídeo y vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494633"
---
# <a name="combining-video-capture-and-preview"></a>Combinación de captura de vídeo y vista previa

En las secciones anteriores se describe cómo capturar vídeo en varios formatos de archivo. En la sección de vista previa del [vídeo](previewing-video.md) se describe cómo crear un gráfico de vista previa dinámica. Sin embargo, muchas aplicaciones deben hacerlo a la vez. Para compilar una vista previa combinada y un gráfico de escritura de archivos, solo tiene que hacer dos llamadas a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



En este código, el generador de gráficos de captura oculta algunos detalles:

-   Si el filtro de captura tiene un PIN de vista previa o un puerto de vídeo, además de un PIN de captura, el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) simplemente representa ambos PIN, tal como se muestra en la siguiente ilustración.

    ![gráfico de captura y vista previa](images/vidcap04.png)

-   Si el filtro solo tiene un PIN de captura, el generador de gráficos de captura usa el filtro de [Smart Tee](smart-tee-filter.md) para dividir el flujo de captura. En la ilustración siguiente se muestra el gráfico con un inteligente tee.

    ![capturar y obtener una vista previa de un gráfico con filtro Smart Tee](images/vidcap05.png)

El filtro Smart Tee tiene un PIN de captura y un PIN de vista previa. Toma un solo flujo de vídeo del filtro de captura y lo divide en dos flujos, uno para la captura y otro para la vista previa. Para mantener el rendimiento en el PIN de captura, el PIN de vista previa quita los fotogramas según sea necesario. También quita las marcas de tiempo de cada muestra antes de entregarlas, por las razones descritas en el tema [filtros de captura de vídeo de DirectShow](directshow-video-capture-filters.md).

Aunque Smart Tee divide el flujo, no duplica físicamente los datos de vídeo. En su lugar, utiliza objetos de ejemplo multimedia personalizados que comparten los búferes. Los ejemplos están marcados como "de solo lectura" para asegurarse de que los filtros de nivel inferior no escriben en los datos.

Si el gráfico de capturas tiene una ventana de vista previa, hay varias cosas que pueden hacer que Filter Graph Manager detenga todo el gráfico, incluida la secuencia de captura:

-   Bloquear el equipo.
-   Presione CTRL + ALT + SUPR en un equipo que sea miembro de un dominio.
-   Ejecutar una aplicación de Direct3D de pantalla completa, como un juego o un protector de pantalla.
-   Cambiar monitores o cambiar la resolución de pantalla.
-   Ejecutar un programa que hace que Windows muestre un cuadro de diálogo de control de cuentas de usuario (UAC). (Windows Vista o posterior).
-   Ejecutar una ventana de DOS de pantalla completa.

Cualquiera de estos eventos puede interrumpir la sesión de captura, lo que podría provocar la pérdida de datos. (Esto es lo que sucede internamente: el representador de vídeo pierde los recursos de Direct3D o DirectDraw que necesita. En el proceso de recuperación de esos recursos, el representador de vídeo debe volver a conectarse con el filtro de nivel superior, lo que hace que el administrador de gráficos de filtro detenga el gráfico).

Dos posibles soluciones a este problema son las siguientes:

-   No incluya una secuencia de vista previa. Sin embargo, tenga en cuenta que el método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) agrega automáticamente una ventana de vista previa cuando el dispositivo de captura tiene un PIN de puerto de vídeo. Consulte [PIN del puerto de vídeo en la captura de archivos](video-port-pins-in-file-capture.md).
-   Use el motor de búfer de secuencia para enviar la secuencia de vista previa a un gráfico en otro proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



