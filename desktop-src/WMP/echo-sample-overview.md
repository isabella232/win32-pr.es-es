---
title: Información general del ejemplo echo
description: Información general del ejemplo echo
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Complementos de Media Player de Windows, información general de ejemplo de eco
- complementos, información general de ejemplo de eco
- Complementos de procesamiento de señal digital, información general de ejemplo de eco
- Complementos DSP, información general de ejemplo de eco
- Ejemplo de complemento DSP de eco, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695391"
---
# <a name="echo-sample-overview"></a>Información general del ejemplo echo

En esta guía se crea un complemento DSP de Windows Media Player que crea un efecto de eco en audio PCM durante la reproducción. Los objetivos del complemento son los siguientes:

-   El complemento procesa únicamente audio PCM de 8 o 16 bits.
-   Admite un tiempo de retraso entre 10 milisegundos (MS) y 2000 MS (2 segundos). Esto representa un intervalo práctico para la mayoría de las aplicaciones.
-   Permite mezclar la señal original con la señal de retraso.
-   Proporciona una implementación de página de propiedades que permite al usuario proporcionar un valor para el tiempo de retraso y un valor para el porcentaje de la señal de retraso en relación con el nivel de señal de audio general.
-   El código se crea modificando el ejemplo de complemento de audio DSP del Asistente para Media Player de Windows.

El ejemplo echo no se incluye en el SDK de Windows Media Player; es un ejemplo que se crea. Para crear el ejemplo echo, debe empezar con el proyecto predeterminado del Asistente para complementos de Media Player de Windows. Puede asignar al proyecto el nombre que desee; en esta documentación se supone que el proyecto se denomina echo. Para obtener más información acerca del uso del asistente, consulte [crear un complemento DSP](building-a-dsp-plug-in.md).

En la sección siguiente se proporciona información general sobre cómo el ejemplo crea un efecto de eco:

-   [Cómo funciona el ejemplo echo](how-the-echo-sample-works.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo echo**](the-echo-sample.md)
</dt> </dl>

 

 




