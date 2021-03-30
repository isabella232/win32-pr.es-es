---
description: Introducción a la programación de aplicaciones de DirectShow
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Introducción a la programación de aplicaciones de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6218a346a7eb9711259c025aef09133ef2e58f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422866"
---
# <a name="introduction-to-directshow-application-programming"></a>Introducción a la programación de aplicaciones de DirectShow

En este artículo se presentan la terminología y los conceptos básicos que se usan en DirectShow. Después de leer esta sección, estará listo para escribir su primera aplicación de DirectShow.

**Filtros y gráficos de filtros**

El bloque de creación de DirectShow es un componente de software denominado *filtro*. Un filtro es un componente de software que realiza alguna operación en una secuencia multimedia. Por ejemplo, los filtros de DirectShow pueden

-   leer archivos
-   obtener vídeo de un dispositivo de captura de vídeo
-   descodificar varios formatos de flujo, como vídeo MPEG-1
-   pasar datos a la tarjeta gráfica o de sonido

Los filtros reciben entradas y generan resultados. Por ejemplo, si un filtro descodifica vídeo MPEG-1, la entrada es la secuencia codificada en MPEG y la salida es una serie de fotogramas de vídeo sin comprimir.

En DirectShow, una aplicación realiza cualquier tarea mediante la conexión de cadenas de filtros juntos, de modo que la salida de un filtro se convierte en la entrada de otro. Un conjunto de filtros conectados se denomina *gráfico de filtro*. Por ejemplo, en el diagrama siguiente se muestra un gráfico de filtros para reproducir un archivo AVI.

![filtrar gráfico para reproducir un archivo AVI](images/avi-filter-graph.png)

El filtro de origen de archivo lee el archivo AVI del disco duro. El filtro de divisor de AVI analiza el archivo en dos flujos, una secuencia de vídeo comprimida y una secuencia de audio. El filtro de descompresor de AVI descodifica los fotogramas de vídeo. El filtro de representador de vídeo dibuja los fotogramas en la pantalla, mediante DirectDraw o GDI. El filtro de dispositivo DirectSound predeterminado reproduce la secuencia de audio mediante DirectSound.

La aplicación no tiene que administrar todo este flujo de datos. En su lugar, los filtros se controlan mediante un componente de alto nivel denominado Filter Graph Manager. La aplicación realiza llamadas API de alto nivel como "Run" (para trasladar datos a través del gráfico) o "STOP" (para detener el flujo de datos). Si necesita más control sobre las operaciones de Stream, puede tener acceso a los filtros directamente a través de las interfaces COM. El administrador de gráficos de filtro también pasa las notificaciones de eventos a la aplicación.

El administrador de gráficos de filtros sirve también a otro propósito: proporciona métodos para que la aplicación genere el gráfico de filtro mediante la conexión de los filtros. (DirectShow también proporciona varios objetos auxiliares que simplifican este proceso. Se describen detalladamente en la documentación).

**Escritura de una aplicación de DirectShow**

En términos generales, hay tres tareas que cualquier aplicación de DirectShow debe realizar. Estos se muestran en el diagrama siguiente.

![aplicación de DirectShow típica](images/fgm.png)

1.  La aplicación crea una instancia de Filter Graph Manager.
2.  La aplicación utiliza el administrador de gráficos de filtro para generar un gráfico de filtro. El conjunto exacto de filtros del gráfico dependerá de la aplicación.
3.  La aplicación utiliza el administrador de gráficos de filtro para controlar el gráfico de filtro y transmitir los datos a través de los filtros. A lo largo de este proceso, la aplicación también responderá a los eventos del administrador de gráficos de filtro.

Una vez completado el procesamiento, la aplicación libera el administrador de gráficos de filtro y todos los filtros.

DirectShow se basa en COM; el administrador de gráficos de filtro y los filtros son objetos COM. Debe tener una descripción general de la programación del cliente COM antes de empezar a programar DirectShow. Hay muchos libros sobre programación COM disponibles.

Para empezar a trabajar con DirectShow, lea el artículo [Cómo reproducir un archivo](how-to-play-a-file.md), que presenta una aplicación de consola simple para reproducir un archivo de vídeo. En la sección [sobre DirectShow](about-directshow.md) se explica con más detalle la arquitectura de DirectShow, mientras que la sección que [usa DirectShow](using-directshow.md) examina los escenarios principales que admite DirectShow, como la captura, la edición de vídeo, la reproducción de DVD y el televisor.

 

 



