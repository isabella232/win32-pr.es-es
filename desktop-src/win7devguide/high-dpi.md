---
title: Configuración elevada de ppp
description: .
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adad7c986c7083ab2327f0c8de0bd2cace5ef20a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078156"
---
# <a name="high-dpi"></a>Configuración elevada de ppp

A medida que las tecnologías de visualización avanzan, los fabricantes han aumentado el número de píxeles admitidos por sus pantallas. Aunque el texto, las imágenes y los elementos de la interfaz de usuario parecen mucho más nítidos y legibles en pantallas de alta resolución, el sistema operativo debe escalarse verticalmente para admitir la experiencia visual. de lo contrario, todo es más pequeño.

Windows 7 admite pantallas de *PPP* altas. Los datos de mercado sugieren que las implementaciones de pantallas de *PPP* altas (120-144 puntos por pulgada (PPP)) aumentarán en el período de tiempo de Windows 7. Cuando se ejecutan soluciones nativas en estas pantallas, muchas aplicaciones aparecen muy pequeñas a menos que utilicen un valor de *PPP alto*. Algunas aplicaciones (por ejemplo, Windows Internet Explorer) tienen características de escalado de fuentes que permiten a los usuarios acercar y alejar, pero muchas aplicaciones no. La característica de *PPP alta* en Windows 7:

-   Garantiza que las experiencias de Windows y de la aplicación sean óptimas en el hardware estándar (la configuración de *PPP* está optimizada para que coincida con las capacidades del hardware).
-   Permite que el shell de Windows y otras aplicaciones basadas en Windows tengan un aspecto correcto con diferentes configuraciones de *PPP* .
-   Respeta la configuración de *PPP* predeterminada en función de las especificaciones de hardware y las capacidades.
-   Permite a los usuarios personalizar la configuración de *PPP* sin necesidad de reiniciar.
-   Garantiza que la pantalla se establezca siempre en resolución nativa.

La característica de ajuste de escala de *PPP* de Windows escala las fuentes y los elementos de la interfaz de usuario (como botones, iconos y campos de entrada) en un porcentaje calculado, tal y como se especifica en la configuración de *PPP* . Esto es diferente del escalado que se produce cuando se reduce la resolución de pantalla. En el caso del ajuste de escala de *PPP* , Windows proporciona fuentes y elementos de la interfaz de usuario que se dibujan con más píxeles, lo que da lugar a una experiencia de Windows mayor, mayor fidelidad y más nítida. Las aplicaciones de terceros de Windows pueden aprovechar la configuración de *PPP alta* y ajustar la interfaz de usuario en consecuencia, declarando a su vez el reconocimiento de *PPP elevado* . Los desarrolladores de aplicaciones ya no deben suponer que 96 PPP es la solución ideal para todas las aplicaciones.

Para obtener más información acerca de los *PPP altos* y la escritura de aplicaciones que tienen un reconocimiento de *PPP alto* , consulte [alta resolución](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 