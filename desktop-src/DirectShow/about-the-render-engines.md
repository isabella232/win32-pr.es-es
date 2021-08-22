---
description: Acerca de los motores de representación
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Acerca de los motores de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a398cbe342ed2e92fc23e7da034dd69cae492208e3201b3419b3999594a135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664390"
---
# <a name="about-the-render-engines"></a>Acerca de los motores de representación

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En este artículo se describe [DirectShow Editing Services](directshow-editing-services.md) (DES) representa un proyecto de edición de vídeo.

En DES, un proyecto se representa como una escala de tiempo. La escala de tiempo es útil porque simplifica las tareas más comunes en la edición de vídeo, como reorganizar los clips de origen y agregar efectos de vídeo. La DirectShow de flujo de datos, por otro lado, requiere un gráfico de filtro. Por lo tanto, para representar el proyecto, debe traducir una escala de tiempo en un gráfico de filtros. El componente que lo hace se denomina motor *de representación*. DirectShow proporciona dos motores de representación:

-   Motor de representación básico: crea un gráfico de filtro que proporciona salida sin comprimir.
-   Motor de representación inteligente: crea un gráfico de filtro que proporciona salida comprimida.

El motor de representación inteligente usa la recompresión inteligente para mejorar el rendimiento. Con la recompresión inteligente, los archivos de origen solo se comprimen cuando el formato de archivo original difiere del formato de salida final. Si los formatos coinciden, el origen nunca se descomprime. La recompresión inteligente solo se admite para la compresión de vídeo, no para la compresión de audio.

Para obtener una vista previa, use el motor de representación básico. El motor de representación inteligente también puede obtener una vista previa, pero de forma menos eficaz porque tiene que descomprimir la secuencia comprimida. Para escribir archivos, use el motor de representación inteligente si desea una recompresión inteligente. De lo contrario, use el motor de representación básico. La recompresión inteligente puede reducir considerablemente el tiempo que se tarda en escribir el archivo.

> [!IMPORTANT]
> No use el motor de representación inteligente para leer o escribir archivos Windows multimedia.

 

> [!IMPORTANT]
> Ambos motores de representación crean una ventana invisible que procesa mensajes. El subproceso que crea el motor de representación debe tener un bucle de mensajes para enviar mensajes. Además, ese subproceso no debe salir hasta que se liberan el motor de representación y Graph administrador de filtros. De lo contrario, la aplicación podría interbloqueo.

 

Construir el filtro Graph

El gráfico de filtros se basa en dos fases. En la primera fase, el motor de representación crea un "front-end", que es un gráfico de filtro parcial. En el diagrama siguiente se muestra un front-end típico:

![front-end de gráfico de filtro](images/rendeng1.png)

Los subsistemas contienen varios filtros especializados, que el motor de representación ensambla automáticamente. El front-end contiene un pin de salida para cada grupo de la escala de tiempo. Las clavijas de salida proporcionan datos sin comprimir si usa el motor de representación básico o datos comprimidos si usa el motor de representación inteligente.

En el segundo paso, las clavijas de salida están conectadas a filtros de representación. Para la versión preliminar, los filtros de representación son representadores de vídeo y audio. Para la escritura de archivos, los filtros de representación son filtros multiplexor (mux) y filtros de escritor de archivos.

![completar el gráfico de filtros](images/rendeng2.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vista previa de un Project](previewing-a-project.md)
</dt> <dt>

[Escribir un Project en un archivo](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



