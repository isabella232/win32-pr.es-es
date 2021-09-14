---
description: Trabajar con códecs
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Trabajar con códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe6d45608c3d95fee8f67344bdec0fc77431919
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272596"
---
# <a name="working-with-codecs"></a>Trabajar con códecs

Microsoft Windows proporciona varios códecs como componentes del sistema operativo. Los códecs disponibles siempre incluyen aquellos que se incluyen con cualquier versión de DirectX y Reproductor de Windows Media se incluyeron en la versión Windows lanzamiento. Se pueden instalar códecs adicionales cuando se instalan versiones más recientes de DirectX o Reproductor de Windows Media o Windows entornos de ejecución del SDK de Media. Los terceros pueden instalar códecs adicionales en un sistema host; Estos códecs pueden estar diseñados para funcionar solo con una aplicación determinada, o bien pueden admitir el uso general por cualquier DirectShow aplicación.

Los códecs se pueden implementar de tres maneras diferentes:

-   Como vídeo para Windows códec instalable de audio o vídeo de tipo que carga el Administrador de compresión de vídeo (VCM) o el Administrador de compresión de audio (ACM). En general, esta tecnología se considera en desuso y no se recomienda su uso. Los códecs instalables participan en DirectShow gráficos de filtro mediante el filtro contenedor de descompresión AVI.
-   Como filtro DirectShow de datos. Muchos códecs de terceros se implementan como filtros de DirectShow nativos. Uno de estos filtros es el filtro de descompresión MP3 de Descomprimidor Descomprimidor Descomprimidor de De En general, estos filtros se pueden agregar al gráfico de filtros de las maneras habituales. Una excepción a esta regla es que algunos códecs Windows Media™ Audio o Windows Media Video y el códec Microsoft MPEG-4 no se pueden agregar manualmente a un gráfico de filtros. Estos filtros solo se pueden agregar mediante los filtros lector de ASF y escritor de ASF.
-   Como objetos multimedia (DMO) de DirectX. Las DDO son la manera recomendada de implementar códecs, ya que se pueden usar dentro de un gráfico de filtros de DirectShow mediante el filtro contenedor de DMO o de forma independiente en cualquier otra aplicación de streaming no basada en DirectShow. Algunos Windows de audio multimedia y Windows códecs de vídeo multimedia se implementan como DDO. Al igual que con los Windows multimedia, estas DDO no se pueden usar fuera del contexto del SDK Windows Media. Esto significa que, DirectShow, solo se pueden agregar a un gráfico a través de los filtros lector de ASF o escritor de ASF.

En GraphEdit, todos estos tipos diferentes de códecs aparecen juntos en las siguientes categorías:

-   Audio de sonido
-   Vídeo de resalte
-   DirectShow filtro

Sin embargo, muchos de estos códecs están instalados por terceros o por otras aplicaciones de Microsoft o componentes del sistema operativo, y no están diseñados para su uso por otras DirectShow aplicaciones. La lista de códecs visibles en GraphEdit también depende de qué versión de Windows se ejecuta en el sistema host y de qué versión del SDK de DirectShow está instalado.

 

 



