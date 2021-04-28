---
title: Configuración elevada de ppp
description: Configuración elevada de ppp
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c70e44c497f116348e7b42b260f056d593524
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114703"
---
# <a name="high-dpi"></a>Configuración elevada de ppp

A medida que avanzan las tecnologías de visualización, los fabricantes han aumentado el número de píxeles admitidos por sus pantallas. Aunque el texto, las imágenes y los elementos de la interfaz de usuario parecen mucho más nítidos y legibles en las pantallas de alta resolución, el sistema operativo debe escalar verticalmente para admitir la experiencia visual. de lo contrario, todo parece más pequeño.

Windows 7 admite pantallas *con valores altos de PPP.* Los datos de mercado sugieren que las implementaciones de pantallas con valores altos de *PPP* (de 120 a 144 puntos por pulgada (ppp)) aumentarán en el período de tiempo de Windows 7. Al ejecutar resoluciones nativas en estas pantallas, muchas aplicaciones aparecen muy pequeñas a menos que usen *valores altos de PPP.* Algunas aplicaciones (como Windows Internet Explorer) tienen características de escalado de fuentes que permiten a los usuarios acercar y alejar, pero muchas aplicaciones no. La *característica Valores altos de* PPP en Windows 7:

-   Garantiza que las experiencias de windows y de aplicación son óptimas en el hardware estándar (la configuración de *PPP* está optimizada para que coincida con las funcionalidades del hardware).
-   Permite que el Shell de Windows y otras aplicaciones basadas en Windows se vean bien con diferentes *configuraciones de PPP.*
-   Respeta la configuración predeterminada *de PPP* en función de las especificaciones y funcionalidades de hardware.
-   Permite a los usuarios personalizar *la configuración de PPP* sin reiniciar.
-   Garantiza que la pantalla siempre está establecida en resolución nativa.

La característica de escalado *de PPP* de Windows escala las fuentes y los elementos de la interfaz de usuario (como botones, iconos y campos de entrada) por un porcentaje calculado, según lo especificado por la configuración *de PPP.* Esto es diferente del escalado que se produce cuando se reduce la resolución de pantalla. En el caso del escalado de *PPP,* Windows proporciona fuentes y elementos de la interfaz de usuario que se dibujan con más píxeles, lo que da lugar a una mayor fidelidad y una experiencia de Windows más clara. Las aplicaciones de Windows de terceros pueden aprovechar la configuración de valores altos de *PPP* y ajustar la interfaz de usuario en consecuencia, declarándose con reconocimiento de valores altos *de PPP.* Los desarrolladores de aplicaciones ya no deben asumir que 96 ppp es la resolución ideal para todas las aplicaciones.

Para obtener más información sobre *valores altos de PPP* y sobre cómo escribir aplicaciones que tienen en cuenta valores altos de *PPP,* vea [Valores altos de PPP.](../hidpi/high-dpi-desktop-application-development-on-windows.md)

 

 
