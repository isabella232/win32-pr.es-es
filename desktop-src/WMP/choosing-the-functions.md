---
title: Elección de las funciones
description: Elección de las funciones
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Máscaras móviles de Windows Media Player, funciones para audio
- máscaras, funciones para audio
- crear máscaras, funciones para audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419055"
---
# <a name="choosing-the-functions"></a>Elección de las funciones

La finalidad de esta máscara es proporcionar la funcionalidad básica para reproducir audio. Se usarán las siguientes funciones:



| Función                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PlayPause o PlayPauseStop\* | El inicio del elemento multimedia es de importancia primordial. Si va a crear una máscara para Windows Media Player 10 Mobile o posterior, debe utilizar PlayPauseStop. Si está trabajando con una versión anterior de Windows Media Player Mobile, debe usar PlayPause. Ambas funciones ofrecen la funcionalidad agregada de pausar, pero solo PlayPauseStop permite detener una difusión en directo cuando no está disponible la funcionalidad de pausa. |
| Stop                         | Querrá agregar STOP para detener la reproducción del elemento. Si va a crear una máscara para Windows Media Player 10 Mobile o posterior, la función PlayPauseStop ya proporciona esta funcionalidad.                                                                                                                                                                                                                                          |
| Siguientes                         | Si tiene una lista de reproducción, querrá poder elegir el elemento siguiente. Lo necesita para la navegación básica de los medios digitales.                                                                                                                                                                                                                                                                                                       |
| Anterior                         | Aunque podría usar Next para desplazarse por la lista de reproducción hasta que llegó al principio, al agregar Prev, se facilitará que el usuario se desplace hacia atrás y hacia delante al navegar por la lista de reproducción.                                                                                                                                                                                                                                   |
| VolumeUp o VolumeDown\*     | Querrá proporcionar al usuario la capacidad de activar o desactivar el volumen.                                                                                                                                                                                                                                                                                                                                                    |



 

\*Disponible para Windows Media Player 10 Mobile o posterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de máscara**](skin-guide.md)
</dt> </dl>

 

 




