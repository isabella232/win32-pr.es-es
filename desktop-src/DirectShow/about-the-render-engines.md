---
description: Acerca de los motores de representación
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Acerca de los motores de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537828"
---
# <a name="about-the-render-engines"></a>Acerca de los motores de representación

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En este artículo se describe cómo los [servicios de edición de DirectShow](directshow-editing-services.md) (des) representan un proyecto de edición de vídeo.

En DES, un proyecto se representa como una escala de tiempo. La escala de tiempo es útil porque simplifica las tareas más comunes en la edición de vídeo, como la reorganización de clips de origen y la adición de efectos de vídeo. La arquitectura de la secuencia de DirectShow, por otro lado, requiere un gráfico de filtro. Por lo tanto, para representar el proyecto, debe traducir una escala de tiempo en un gráfico de filtros. El componente que lo lleva a cabo se denomina *motor de representación*. DirectShow proporciona dos motores de representación:

-   Motor de representación básico: crea un gráfico de filtro que proporciona una salida sin comprimir.
-   Smart Render Engine: crea un gráfico de filtro que entrega la salida comprimida.

El motor de representación inteligente utiliza la recompresión inteligente para mejorar el rendimiento. Con la recompresión inteligente, los archivos de origen se vuelven a comprimir solo cuando el formato de archivo original difiere del formato de salida final. Si los formatos coinciden, el origen nunca se descomprimirá. La recompresión inteligente solo se admite para la compresión de vídeo, no para la compresión de audio.

Para la versión preliminar, use el motor de representación básico. El motor de representación inteligente también puede obtener una vista previa, pero es menos eficaz porque tiene que descomprimir el flujo comprimido. Para escribir archivos, use el motor de representación inteligente si desea volver a comprimir inteligente. De lo contrario, use el motor de representación básico. La recompresión inteligente puede reducir en gran medida el tiempo que se tarda en escribir el archivo.

> [!IMPORTANT]
> No utilice el motor de representación inteligente para leer o escribir archivos de Windows Media.

 

> [!IMPORTANT]
> Ambos motores de representación crean una ventana invisible que procesa los mensajes. El subproceso que crea el motor de representación debe tener un bucle de mensajes para enviar los mensajes. Además, ese subproceso no debe salir hasta que se liberen el motor de representación y el administrador de gráficos de filtro. De lo contrario, la aplicación podría bloquearse.

 

Construir el gráfico de filtro

El gráfico de filtro se crea en dos fases. En la primera fase, el motor de representación construye un "front-end", que es un gráfico de filtro parcial. En el diagrama siguiente se muestra un front-end típico:

![Front-end de gráfico de filtro](images/rendeng1.png)

Los subsistemas contienen varios filtros especializados, que el motor de representación ensambla automáticamente. El front-end contiene un PIN de salida para cada grupo de la escala de tiempo. Los pin de salida proporcionan datos sin comprimir si usa el motor de representación básico o datos comprimidos si usa el motor de representación inteligente.

En el segundo paso, los pin de salida se conectan a los filtros de representación. En la versión preliminar, los filtros de representación son representadores de audio y vídeo. En el caso de la escritura de archivos, los filtros de representación son filtros de multiplexor (MUX) y filtros de escritura de archivos.

![finalización del gráfico de filtros](images/rendeng2.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener una vista previa de un proyecto](previewing-a-project.md)
</dt> <dt>

[Escribir un proyecto en un archivo](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



