---
title: Configuración del registro de esquema personalizado
description: Configuración del registro de esquema personalizado
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, configuración del registro de esquema personalizado
- Media Player de Windows, esquemas
- Media Player de Windows, registro
- registro, configuración de esquema personalizado
- registro, esquemas
- registro, configuración para Windows Media Player
- esquemas
- configuración del registro de esquema personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075312"
---
# <a name="custom-scheme-registry-settings"></a>Configuración del registro de esquema personalizado

Los esquemas son protocolos personalizados. Windows Media Player mantiene una lista de esquemas del registro en el equipo del usuario. Cuando el usuario intenta reproducir un archivo multimedia digital, el reproductor comprueba primero si el SDK de Windows Media Format es compatible con el esquema. Si no es así, el reproductor comprueba el esquema con la lista del registro. Si se encuentra una coincidencia, el reproductor comprueba un valor que indica qué tecnología subyacente, o *tiempo de ejecución* (como Microsoft DirectShow o el SDK de Windows Media Format), se puede usar para reproducir el archivo. Si no se encuentra ninguna coincidencia, el reproductor presenta al usuario un cuadro de diálogo de advertencia que solicita permiso al usuario para intentar reproducir el archivo. Si transmite por secuencias archivos multimedia digitales mediante un esquema de protocolo personalizado, puede evitar que esta advertencia aparezca en el equipo del usuario registrando el esquema y proporcionando un valor para el tiempo de ejecución.

La lista de esquemas se mantiene como un conjunto de claves del registro que coinciden con los esquemas registrados, sin los dos puntos y las dos barras diagonales (://). Por ejemplo, la clave para el esquema wmhtml://, que se usa para transmitir multimedia enriquecidas, se denomina "wmhtml". Se mantiene una lista independiente para el equipo local y para cada usuario. En el caso del equipo local, las claves de esquema son subclaves de la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimedia \\ WMPlayer \\ schemes\\**

Por ejemplo, la clave del esquema wmhtml://para el equipo local es:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimedia \\ WMPlayer \\ schemes \\ wmhtml**

Para cambiar los valores de esta clave o para crear una nueva subclave, el usuario actual debe ser administrador del equipo.

Para usuarios individuales, las claves de esquema son subclaves de la siguiente clave del registro:

**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ schemes\\**

Por ejemplo, la clave del esquema wmhtml://para el usuario actual es:

**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ schemes \\ wmhtml**

Al comprobar los esquemas registrados, el reproductor comprueba primero los valores ubicados en **HKEY \_ local \_ Machine**. Si no se encuentra ninguno para el esquema actual, el reproductor comprueba después los valores de **HKEY \_ Current \_ User**. Si no se encuentra ninguno para el esquema actual, el reproductor muestra la advertencia al usuario.

Cada subclave de esquema puede contener uno de los siguientes valores posibles para el *tiempo de ejecución*.



| Value | Descripción                                |
|-------|--------------------------------------------|
| 6     | Se representa mediante el SDK de Windows Media Format. |
| 7     | Se representa mediante Microsoft DirectShow.         |



 

Cambiar el valor *en tiempo de ejecución* de un esquema compatible con el SDK de Windows Media Format no tendrá ningún efecto. El reproductor siempre usará el SDK de Windows Media Format como tiempo de ejecución para los esquemas compatibles con el SDK de Windows Media Format. Este valor del registro está diseñado para permitir la configuración en tiempo de ejecución para esquemas personalizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro**](registry-settings.md)
</dt> </dl>

 

 




