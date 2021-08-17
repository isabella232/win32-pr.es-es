---
title: Funcionamiento del Administrador de compresión de audio
description: Funcionamiento del Administrador de compresión de audio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimedia, administrador de compresión de audio (ACM)
- audio, administrador de compresión de audio (ACM)
- administrador de compresión de audio (ACM), acerca de
- ACM (administrador de compresión de audio), acerca de
- administrador de compresión de audio (ACM), controladores de códecs
- ACM (administrador de compresión de audio), controladores de códec
- administrador de compresión de audio (ACM), controladores de convertidor de formato
- ACM (administrador de compresión de audio), controladores de convertidor de formato
- administrador de compresión de audio (ACM), controladores de filtro
- ACM (administrador de compresión de audio), controladores de filtro
- administrador de compresión de audio (ACM), controladores de sonido
- ACM (administrador de compresión de audio), controladores de sonido
- administrador de compresión de audio (ACM), controladores de descompresión
- ACM (administrador de compresión de audio), controladores de descompresión
- controladores de códecs
- controladores de convertidor de formato
- controladores de filtro
- controladores de transporte
- controladores de descompresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb3d94feee3da290bf9c1cc90cab92f2aade083effd8a01cb17906c22e0f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141016"
---
# <a name="how-the-audio-compression-manager-works"></a>Funcionamiento del Administrador de compresión de audio

El ACM usa enlaces de interfaz de controlador existentes para invalidar el algoritmo de asignación predeterminado para dispositivos de audio de onda. Esto permite que el ACM intercepte las llamadas abiertas del dispositivo. Una vez interceptada una llamada, el ACM puede realizar diversas tareas para procesar los datos de audio, como insertar un descomprimidor externo en la secuencia.

El ACM administra los siguientes tipos de controladores:

-   Controladores de descompresión y descompresión (códec)
-   Controladores de convertidor de formato
-   Controladores de filtro

Los descompresores y los descompresores cambian un tipo de formato a otro. Por ejemplo, un descomprimidor o descomprimidor puede cambiar un archivo PCM (pulse Code Estadicón) a un archivo ADPCM (Adaptive Differential Pulse Code Adaptive). Los convertidores de formato cambian el formato, pero no el tipo de datos. Por ejemplo, un convertidor puede cambiar datos de 44 kHz de 16 bits a datos de 44 kHz y 8 bits. Los filtros no cambian el formato de los datos, pero cambian los datos de audio de forma de onda de alguna manera. Por ejemplo, un filtro podría combinar un flujo de datos y un eco de sí mismo. Un único controlador ACM, o una etiqueta de filtro o etiqueta de formato dentro de un controlador, también puede admitir combinaciones de los tipos anteriores.

Para la salida de audio de forma de onda, el ACM pasa cada búfer de datos al convertidor a medida que llegan. El convertidor descomprime los datos y devuelve los datos descomprimidos al ACM en un búfer de "sombra". A continuación, el ACM pasa el búfer de sombra descomprimido al controlador de audio de forma de onda. El ACM asigna los búferes de sombra cada vez que recibe un mensaje de preparación.

Para la entrada de audio de forma de onda, el ACM pasa búferes de sombra vacíos al controlador. Usa una tarea en segundo plano para recibir una notificación después de que el controlador haya rellenado el búfer de sombras. A continuación, el ACM pasa los búferes al controlador para la compresión. Una vez finalizada la compresión, el controlador pasa los datos a la aplicación.

 

 




