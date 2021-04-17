---
description: .
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Interfaz de usuario: reconocimiento de valores altos de PPP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e93aeed452f421e8e38df8d6d75f6bbe1f97cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717300"
---
# <a name="user-interface---high-dpi-awareness"></a>Interfaz de usuario: reconocimiento de valores altos de PPP

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes** -Windows XP Windows \| vista Windows \| 7  

## <a name="feature-impact"></a>Impacto en las características

**Gravedad** : medio  
**Frecuencia** : medio  

## <a name="description"></a>Descripción

El objetivo es animar a los usuarios finales a establecer sus visualizaciones en la resolución nativa y usar PPP en lugar de la resolución de pantalla para cambiar el tamaño del texto y las imágenes que se muestran. Windows 7 puede detectar automáticamente y configurar un valor de PPP predeterminado en las instalaciones limpias en los equipos configurados por los OEM mediante la configuración de PPP. Hay herramientas que puede usar para diseñar aplicaciones que tienen un reconocimiento de PPP elevado para garantizar los resultados más legibles.

Hemos agregado dos nuevas características de PPP altas a Windows 7:

-   Configuración de PPP por usuario (antes por equipo)
-   Cambiar PPP sin reinicio (cierre de sesión o inicio de sesión sigue siendo necesario)

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

Es probable que las aplicaciones que no controlan el uso de mayúsculas altas de PPP muestren artefactos visuales, como:

-   Recorte de la interfaz de usuario o texto por otros elementos de la interfaz de usuario
-   Tamaños de fuente incoherentes
-   Ius de pantalla
-   Desenfoque de texto o interfaz de usuario
-   Arrastre y colocación rotos u otras entradas
-   Representación parcial de las aplicaciones DX en pantalla completa

## <a name="solution"></a>Solución

Para hacer que las aplicaciones sean compatibles con PPP:

1.  Realice una prueba funcional de alto nivel, incluida la instalación y desinstalación en la siguiente configuración:

    | Configuración                                              | Qué se debe tener presente                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024x768 a 120 ppp (125% de escala)                    | Esta es una resolución eficaz de ~ 800x600, por lo que debe buscar la interfaz de usuario recortada de los problemas de pantalla o diseño. Busque también pixelado bitmaps & iconos.                         |
    | 1600x1200 @144 PPP (escala del 150%)                    | Interfaz de usuario borrosa. Compruebe que todas las operaciones del mouse funcionan, especialmente arrastre & operaciones de colocar. Compruebe también que los modos de pantalla completa funcionan correctamente.                                     |
    | 1600x1200 @ 144 ppp con la virtualización de PPP deshabilitada | A menudo, los botones y la interfaz de usuario no se escalarán en relación con el texto más grande & habrá un recorte significativo del texto. Busque problemas de diseño en los iconos generales & pixelado bitmats &. |

    

     

2.  Anote todos los problemas encontrados, incluidos la configuración de la ubicación, la resolución de pantalla y el PPP, y cómo se comporta la aplicación en las demás configuraciones de PPP/resolución para integridad
3.  Comprobar cada problema con los problemas de codificación de PPP comunes
4.  Evalúe el costo de que la aplicación sea totalmente compatible con el reconocimiento de PPP
5.  Haga una lista de los activos de valores altos de PPP necesarios (por ejemplo, botones, iconos)
6.  Trabajar y corregir la lista de problemas de PPP encontrados en el paso 1
7.  Integre los nuevos recursos del paso 5
8.  Declarar el reconocimiento de PPP de la aplicación

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Vuelva a ejecutar la evaluación de reconocimiento de PPP y compruebe que los problemas se han corregido.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Desarrollo de aplicaciones de escritorio de alto nivel de PPP en Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Póngase en contacto con para obtener preguntas técnicas:**<disup@microsoft.com>

 

 
