---
description: Introducción a la programación DirectShow aplicaciones
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Introducción a la programación DirectShow aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a448d49939e69b7c8a3b244b27a91a93eaf941eebf1960b7b2a53e4ad9137341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823524"
---
# <a name="introduction-to-directshow-application-programming"></a>Introducción a la programación DirectShow aplicaciones

En este artículo se presentan la terminología y los conceptos básicos que se usan en DirectShow. Después de leer esta sección, estará listo para escribir su primera DirectShow aplicación.

**Filtros y gráficos de filtros**

El bloque de creación de DirectShow es un componente de software denominado *filtro*. Un filtro es un componente de software que realiza alguna operación en una secuencia multimedia. Por ejemplo, DirectShow filtros pueden

-   leer archivos
-   obtener vídeo de un dispositivo de captura de vídeo
-   descodificar varios formatos de secuencia, como vídeo MPEG-1
-   pasar datos a la tarjeta de gráficos o sonido

Los filtros reciben la entrada y generan la salida. Por ejemplo, si un filtro descodifica vídeo MPEG-1, la entrada es la secuencia codificada en MPEG y la salida es una serie de fotogramas de vídeo sin comprimir.

En DirectShow, una aplicación realiza cualquier tarea conectando cadenas de filtros, de modo que la salida de un filtro se convierta en la entrada de otro. Un conjunto de filtros conectados se denomina gráfico *de filtros.* Por ejemplo, en el diagrama siguiente se muestra un gráfico de filtro para reproducir un archivo AVI.

![gráfico de filtro para reproducir un archivo avi](images/avi-filter-graph.png)

El filtro Origen de archivo lee el archivo AVI del disco duro. El filtro divisor AVI analiza el archivo en dos secuencias, una secuencia de vídeo comprimida y una secuencia de audio. El filtro de descompresión AVI descodifica los fotogramas de vídeo. El filtro Representador de vídeo dibuja los fotogramas en la pantalla mediante DirectDraw o GDI. El filtro Dispositivo Direct Sound predeterminado reproduce la secuencia de audio mediante Direct Sound.

La aplicación no tiene que administrar todo este flujo de datos. En su lugar, los filtros se controlan mediante un componente de alto nivel denominado Filter Graph Manager. La aplicación realiza llamadas API de alto nivel, como "Ejecutar" (para mover datos a través del gráfico) o "Detener" (para detener el flujo de datos). Si necesita más control sobre las operaciones de flujo, puede acceder a los filtros directamente a través de interfaces COM. Filter Graph Manager también pasa notificaciones de eventos a la aplicación.

Filter Graph Manager también sirve para otro propósito: proporciona métodos para que la aplicación compile el gráfico de filtros mediante la conexión de los filtros. (DirectShow también proporciona varios objetos auxiliares que simplifican este proceso. Se describen exhaustivamente en la documentación).

**Escritura de una DirectShow aplicación**

En términos generales, hay tres tareas que cualquier DirectShow debe realizar. Estos se muestran en el diagrama siguiente.

![aplicación directshow típica](images/fgm.png)

1.  La aplicación crea una instancia de Filter Graph Manager.
2.  La aplicación usa filter Graph Manager para crear un gráfico de filtros. El conjunto exacto de filtros del gráfico dependerá de la aplicación.
3.  La aplicación usa filter Graph Manager para controlar el gráfico de filtros y transmitir datos a través de los filtros. A lo largo de este proceso, la aplicación también responderá a los eventos del Administrador de Graph filtros.

Cuando se completa el procesamiento, la aplicación libera el Administrador de Graph y todos los filtros.

DirectShow se basa en COM; El Administrador Graph filtros y los filtros son todos objetos COM. Debe tener un conocimiento general de la programación del cliente COM antes de empezar a programar DirectShow. Hay muchos libros disponibles sobre la programación COM.

Para empezar a trabajar con DirectShow, lea el artículo [Cómo](how-to-play-a-file.md)reproducir un archivo , que presenta una aplicación de consola sencilla para reproducir un archivo de vídeo. En la sección Acerca de [DirectShow](about-directshow.md) se explica la arquitectura de DirectShow con más detalle, mientras que la sección Uso de [DirectShow](using-directshow.md) examina los escenarios principales compatibles con DirectShow, como la captura, la edición de vídeo, la reproducción de DVD y la televisión.

 

 



