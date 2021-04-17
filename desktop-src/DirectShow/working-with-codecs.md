---
description: Trabajar con códecs
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Trabajar con códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe6d45608c3d95fee8f67344bdec0fc77431919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666764"
---
# <a name="working-with-codecs"></a>Trabajar con códecs

Microsoft Windows proporciona varios códecs como componentes del sistema operativo. Los códecs disponibles siempre incluyen los que se incluyen con la versión de DirectX y Windows Media Player se incluyó en la versión de Windows. Se pueden instalar códecs adicionales cuando se instalan versiones más recientes de DirectX o Windows Media Player o los tiempos de ejecución del SDK de Windows Media. Los terceros pueden instalar códecs adicionales en un sistema host; Estos códecs pueden estar diseñados para funcionar solo con una aplicación determinada, o bien pueden ser compatibles con el uso general de cualquier aplicación de DirectShow.

Los códecs se pueden implementar de tres maneras diferentes:

-   Como vídeo de tipo Windows-Type audio o códec instalable de vídeo cargado por el administrador de compresión de vídeo (VCM) o el administrador de compresión de audio (ACM). En general, esta tecnología se considera en desuso y no se recomienda su uso. Los códecs instalables participan en gráficos de filtros de DirectShow mediante el filtro de contenedor de descompresor de AVI.
-   Como filtro de DirectShow. Muchos códecs de terceros se implementan como filtros de DirectShow nativos. Uno de estos filtros es el filtro de descompresor de MP3 de Frauenhofer. En general, estos filtros se pueden agregar al gráfico de filtros de la manera habitual. Una excepción a esta regla es que algunos códecs de Windows Media™ Audio o Windows Media Video y el códec MPEG-4 de Microsoft no se pueden agregar manualmente a un gráfico de filtro. Estos filtros solo los puede Agregar el lector ASF y los filtros de escritura ASF.
-   Como objetos multimedia de DirectX (DMOs). DMOs son la manera recomendada de implementar códecs, ya que se pueden usar en un gráfico de filtros de DirectShow mediante el filtro de contenedor de DMO, o bien de forma independiente en cualquier otra aplicación de streaming no basada en DirectShow. Algunos códecs de Windows Media Audio y Windows Media Video se implementan como DMOs. Al igual que con los filtros de Windows Media, estos DMOs no se pueden usar fuera del contexto del SDK de Windows Media. Esto significa que, en DirectShow, solo se pueden agregar a un gráfico a través de los filtros ASF Reader o ASF Writer.

En GraphEdit, todos estos tipos diferentes de códecs aparecen juntos en las siguientes categorías:

-   Compresor de audio
-   Compresor de vídeo
-   Filtro de DirectShow

Muchos de estos códecs, sin embargo, los instalan terceros, o bien otras aplicaciones de Microsoft o componentes del sistema operativo, y no están pensados para que los usen otras aplicaciones de DirectShow. La lista de códecs visibles en GraphEdit también depende de la versión de Windows que se ejecute en el sistema host y de la versión del SDK de DirectShow instalada.

 

 



