---
title: Cómo funciona el administrador de compresión de audio
description: Cómo funciona el administrador de compresión de audio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimedia, administrador de compresión de audio (ACM)
- audio, administrador de compresión de audio (ACM)
- Administrador de compresión de audio (ACM), acerca de
- ACM (Administrador de compresión de audio), acerca de
- Administrador de compresión de audio (ACM), controladores de códecs
- ACM (Administrador de compresión de audio), controladores de códecs
- Administrador de compresión de audio (ACM), controladores de convertidor de formato
- ACM (Administrador de compresión de audio), controladores de convertidor de formato
- Administrador de compresión de audio (ACM), controladores de filtro
- ACM (Administrador de compresión de audio), controladores de filtro
- Administrador de compresión de audio (ACM), controladores de compresores
- ACM (Administrador de compresión de audio), controladores de compresores
- Administrador de compresión de audio (ACM), controladores de descompresor
- ACM (Administrador de compresión de audio), controladores de descompresor
- Controladores de códecs
- Controladores de convertidor de formato
- Controladores de filtro
- Controladores de compresores
- Controladores de descompresor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357253"
---
# <a name="how-the-audio-compression-manager-works"></a>Cómo funciona el administrador de compresión de audio

ACM usa enlaces de interfaz de controlador existentes para invalidar el algoritmo de asignación predeterminado para dispositivos de audio de forma de onda. Esto permite a ACM interceptar las llamadas de apertura del dispositivo. Una vez interceptada una llamada, el ACM puede realizar una serie de tareas para procesar los datos de audio, como insertar un compresor externo o descompresor en la secuencia.

ACM administra los siguientes tipos de controladores:

-   Controladores de compresor y descompresor (codec)
-   Controladores de convertidor de formato
-   Controladores de filtro

Los compresores y descompresores cambian un tipo de formato a otro. Por ejemplo, un compresor o descompresor puede cambiar un archivo PCM (modulación por pulsos de código) a un archivo ADPCM (modulación de código de impulso diferencial adaptativo). Los convertidores de formato cambian el formato, pero no el tipo de datos. Por ejemplo, un convertidor puede cambiar los datos de 44 kHz de 16 bits a los datos de 8 bits a 44-kHz. Los filtros no cambian el formato de los datos, pero cambian los datos de audio de forma de onda de alguna manera. Por ejemplo, un filtro podría combinar un flujo de datos y un eco de sí mismo. Un solo controlador ACM, una etiqueta de filtro o una etiqueta de formato dentro de un controlador, podrían admitir también combinaciones de los tipos anteriores.

En el caso de la salida de audio de forma de onda, ACM pasa cada búfer de datos al convertidor cuando llega. El convertidor descomprime los datos y devuelve los datos descomprimidos a ACM en un búfer "Shadow". A continuación, ACM pasa el búfer de instantáneas descomprimidos al controlador de audio de onda. El ACM asigna los búferes de instantáneas cada vez que recibe un mensaje de preparación.

En el caso de la entrada de audio de onda, ACM pasa búferes de instantáneas vacíos al controlador. Usa una tarea en segundo plano para recibir una notificación una vez que el controlador ha rellenado el búfer de sombra. A continuación, el ACM pasa los búferes al controlador para la compresión. Una vez finalizada la compresión, el controlador pasa los datos a la aplicación.

 

 




