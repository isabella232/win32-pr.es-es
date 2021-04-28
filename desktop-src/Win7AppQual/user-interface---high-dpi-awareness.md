---
description: 'Interfaz de usuario: reconocimiento de valores altos de PPP'
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Interfaz de usuario: reconocimiento de valores altos de PPP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116073"
---
# <a name="user-interface---high-dpi-awareness"></a>Interfaz de usuario: reconocimiento de valores altos de PPP

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes:** Windows XP \| Windows Vista Windows \| 7  

## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** media  
**Frecuencia:** media  

## <a name="description"></a>Descripción

El objetivo es animar a los usuarios finales a establecer sus pantallas en resolución nativa y usar PPP en lugar de la resolución de pantalla para cambiar el tamaño del texto y las imágenes mostrados. Windows 7 puede detectar y configurar automáticamente un valor predeterminado de PPP en las máquinas configuradas por sus OEM mediante la configuración de PPP. Hay herramientas que puede usar para ayudar a diseñar aplicaciones que tienen en cuenta valores altos de PPP con el fin de garantizar los resultados más legibles.

Hemos agregado dos nuevas características de valores altos de PPP a Windows 7:

-   Configuración de PPP por usuario (anteriormente por equipo)
-   Cambio de PPP sin reiniciar (todavía se requiere cierre de sesión o inicio de sesión)

## <a name="manifestation-of-impact"></a>Demostración del impacto

Es probable que las aplicaciones que no controlan el caso de valores altos de PPP expondrán artefactos visuales, entre los que se incluyen:

-   Recorte de la interfaz de usuario o texto por otros elementos de la interfaz de usuario
-   Tamaños de fuente incoherentes
-   IOS fuera de la pantalla
-   Desenfoque de texto o interfaz de usuario
-   Arrastrar y colocar rotos u otras entradas
-   Representación de aplicaciones DX de pantalla completa parcialmente fuera de la pantalla

## <a name="solution"></a>Solución

Para que las aplicaciones tenga en cuenta ppp:

1.  Realice una prueba funcional de alto nivel, incluida la instalación y desinstalación en la siguiente configuración:

    | Parámetro                                              | Qué se debe tener presente                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024 x 768 a 120 PPP (escalado del 125 %)                    | Se trata de una resolución efectiva de ~800 x 600, así que busque la interfaz de usuario recortada de la pantalla o los problemas de diseño. Busque también mapas de bits con forma de & iconos.                         |
    | 1600 x 1200 @144 PPP (escalado del 150 %)                    | Interfaz de usuario desenfoque. Compruebe que todas las operaciones del mouse funcionan, especialmente para arrastrar & operaciones de colocación. Compruebe también que los modos de pantalla completa funcionan correctamente.                                     |
    | 1600x1200 @ 144 PPP con la virtualización de PPP deshabilitada | A menudo, los botones y la interfaz de usuario no se escalan en relación con el texto & habrá un recorte de texto significativo. Busque problemas de diseño en general & bits con forma de & iconos. |

    

     

2.  Anote todos los problemas encontrados, incluida la ubicación, la resolución de pantalla y la configuración de PPP, así como el comportamiento de la aplicación en las demás configuraciones de PPP/Resolución para que sea completa.
3.  Comprobar cada problema con los problemas comunes de codificación de PPP
4.  Evaluar el costo de hacer que la aplicación sea totalmente compatible con PPP
5.  Crear una lista de los recursos de valores altos de PPP necesarios (por ejemplo, botones o iconos)
6.  Solucionar y corregir la lista de problemas de PPP que se encuentran en el paso 1
7.  Integración de los nuevos recursos del paso 5
8.  Declaración de la aplicación compatible con PPP

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Vuelva a ejecutar la evaluación de reconocimiento de PPP y compruebe que los problemas se han corregido.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Desarrollo de aplicaciones de escritorio con valores altos de PPP en Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Póngase en contacto con para preguntas técnicas:**<disup@microsoft.com>

 

 
