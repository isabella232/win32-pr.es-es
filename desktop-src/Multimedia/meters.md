---
title: Metros
description: Metros
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- mezcladores de audio, controles
- mezcladores de audio, medidores
- mezcladores, controles
- mezcladores, medidores
- controles de medidor
- MIXERCONTROLDETAILS_BOOLEAN estructura
- MIXERCONTROLDETAILS_SIGNED estructura
- MIXERCONTROLDETAILS_UNSIGNED estructura
- Control booleano
- control de pico
- control firmado
- control sin signo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372133"
---
# <a name="meters"></a>Metros

Los controles de medidor miden los datos que pasan a través de una línea de audio. Estos controles usan las estructuras [**\_ BOOLEAN MIXERCONTROLDETAILS,**](/previous-versions//dd757295(v=vs.85)) [**MIXERCONTROLDETAILS \_ SIGNED**](/previous-versions//dd757297(v=vs.85))y [**MIXERCONTROLDETAILS \_ UNSIGNED**](/previous-versions//dd757298(v=vs.85)) para recuperar y establecer propiedades de control. En la tabla siguiente se describen los tipos de medidores.



| Control  | Descripción                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Booleano  | Mide si un valor entero es FALSE/OFF (cero) o TRUE/ON (distinto de cero).                                                                            |
| Peak     | Mide la desviación de 0 en las direcciones positiva y negativa. El intervalo de valores enteros para el medidor máximo es de -32 768 a 32 767. |
| Firmado   | Mide los valores enteros del intervalo de –231 a (231 – 1). El controlador mezclador define los límites de este medidor.                                     |
| Sin signo | Mide los valores enteros del intervalo de 0 a (232 – 1). El controlador mezclador define los límites de este medidor.                                        |



 

 

 