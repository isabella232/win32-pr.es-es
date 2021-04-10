---
title: La interfaz de usuario perimetral se suprime en escenarios "in-in-in" e "inercia"
description: La interfaz de usuario perimetral se suprime en escenarios "in-in-in" e "inercia"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269331"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>La interfaz de usuario perimetral se suprime en escenarios "in-in-in" e "inercia"

## <a name="platform"></a>Plataforma

<dl> Clientes-Windows 8.1  
</dl>

## <a name="description"></a>Descripción

Hay algunos casos en los que los usuarios pueden invocar involuntariamente la interfaz de usuario perimetral (accesos, barra de aplicaciones, conmutación de aplicaciones). Hemos introducido una característica que permite a los desarrolladores diseñar su interfaz de usuario para toda la pantalla sin necesidad de prestaciones (por ejemplo, bordes) para evitar que el usuario golpee accidentalmente los bordes.

Hay dos casos en los que es posible que se produzcan con más frecuencia los deslizantes de la arista involuntaria:

-   En el movimiento panorámico rápido, la velocidad y el imprecisión de la interacción pueden ocasionar ocasionalmente que entren en el borde de la pantalla.
-   Si los usuarios salen y vuelven a entrar rápidamente en el área de la pantalla mientras escriben entradas manuscritas con el dedo, por ejemplo, en una aplicación de pintura, este comportamiento en espera puede desencadenar erróneamente la interfaz de usuario perimetral e interrumpir la experiencia del usuario.

Para mejorar la experiencia del usuario y del desarrollador, la interfaz de usuario perimetral ahora se suprimirá en dos instancias específicas:

-   Cuando un usuario está en movimiento panorámico en una aplicación que admite la inercia DManip y desliza el dedo fuera de la pantalla mientras se está produciendo la inercia, la interfaz de usuario perimetral no se invocará dentro de una ventana de tiempo de espera.
-   En los dispositivos certificados, cuando un usuario se desliza rápidamente desde la pantalla hacia fuera de la pantalla y viceversa, dentro de determinados parámetros, no se invocará la interfaz de usuario perimetral.

## <a name="manifestations"></a>Manifestaciones

Los usuarios que se deslizan rápidamente con el borde mientras se usa una aplicación verán una disminución en la invocación del perímetro involuntaria.

## <a name="solution"></a>Solución

Los desarrolladores deben tener en cuenta estos factores y deben poder usar la pantalla completa sin temor de que los usuarios desencadenen accidentalmente la interfaz de usuario perimetral mientras interactúan con la aplicación a lo largo del perímetro.

 

 




