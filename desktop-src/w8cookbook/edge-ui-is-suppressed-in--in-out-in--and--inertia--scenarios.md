---
title: La interfaz de usuario de Edge se suprime en escenarios de "entrada y salida" e "inercia".
description: La interfaz de usuario de Edge se suprime en escenarios de "entrada y salida" e "inercia".
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec032fa97f54fc1b1325055c9b02bdebe9e817b0f85971c2e2a7062e93c284c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593965"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>La interfaz de usuario de Edge se suprime en escenarios de "entrada y salida" e "inercia".

## <a name="platform"></a>Plataforma

<dl> Clientes: Windows 8.1  
</dl>

## <a name="description"></a>Descripción

Hay algunos casos en los que los usuarios pueden invocar involuntarlamente la interfaz de usuario de Edge (accesos, barra de aplicaciones, cambio de aplicación). Hemos introducido una característica para permitir que los desarrolladores diseñen su interfaz de usuario para toda la pantalla sin tener que realizar ninguna asequibilidad (por ejemplo, bordes) para evitar que el usuario atrase accidentalmente los bordes.

Hay dos casos que pueden dar lugar con más frecuencia a deslizamientos de borde involuntarios:

-   En el movimiento panorámico rápido, la velocidad y la imprecisión de la interacción pueden hacer que en ocasiones entren desde el borde de la pantalla.
-   Si los usuarios abandonan y vuelven a entrar rápidamente en el área de pantalla mientras se infieren con el dedo, por ejemplo, en una aplicación de dibujo, este comportamiento de entrada puede desencadenar erróneamente la interfaz de usuario de Edge e interrumpir la experiencia del usuario.

Para mejorar la experiencia del usuario y el desarrollador, la interfaz de usuario de Edge ahora se suprimirá en dos instancias específicas:

-   Cuando un usuario se desplaza en movimiento panorámico en una aplicación que admite la inercia de DManip y desliza el dedo fuera de la pantalla mientras se produce la inercia, la interfaz de usuario de Edge no se invocará dentro de una ventana de tiempo de espera.
-   En dispositivos certificados, cuando un usuario desliza rápidamente el dedo desde dentro de la pantalla hacia fuera de la pantalla y hacia atrás dentro (en movimiento) dentro de determinados parámetros, no se invocará la interfaz de usuario de Edge.

## <a name="manifestations"></a>Manifestaciones

Los usuarios que se deslizan rápidamente contra el borde mientras usan una aplicación verán una disminución en la invocación involuntaria del borde.

## <a name="solution"></a>Solución

Los desarrolladores deben tener en cuenta estas mitigaciones y deben poder usar la pantalla completa sin miedo a que los usuarios desencadene accidentalmente la interfaz de usuario de Edge mientras interactúan con la aplicación a lo largo del perímetro.

 

 




