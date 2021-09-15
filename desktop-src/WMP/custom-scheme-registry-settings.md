---
title: Registro de esquemas personalizados Configuración
description: Registro de esquemas personalizados Configuración
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Reproductor de Windows Media,configuración del Registro de esquema personalizado
- Reproductor de Windows Media,schemes
- Reproductor de Windows Media,registry
- registry,custom scheme settings
- registry,schemes
- registry,settings for Reproductor de Windows Media
- esquemas
- configuración del Registro de esquemas personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258924"
---
# <a name="custom-scheme-registry-settings"></a>Registro de esquemas personalizados Configuración

Los esquemas son protocolos personalizados. Reproductor de Windows Media mantiene una lista de esquemas en el Registro en el equipo del usuario. Cuando el usuario intenta reproducir un archivo multimedia digital, el Reproductor comprueba primero si el SDK Windows Media Format admite el esquema. Si no es así, el reproductor comprueba el esquema con la lista del Registro. Si se encuentra una coincidencia, el Reproductor comprueba un valor que indica qué tecnología subyacente o tiempo de ejecución *(como* Microsoft DirectShow o el SDK de formato multimedia de Windows) se pueden usar para reproducir el archivo. Si no se encuentra ninguna coincidencia, el reproductor presenta al usuario un cuadro de diálogo de advertencia que solicita permiso al usuario para intentar reproducir el archivo. Si transmite archivos multimedia digitales mediante un esquema de protocolo personalizado, puede evitar que esta advertencia aparezca en el equipo del usuario registrando el esquema y proporcionando un valor para el tiempo de ejecución.

La lista de esquemas se mantiene como un conjunto de claves del Registro que coinciden con los esquemas registrados, sin los dos puntos y las dos barras diagonales (://). Por ejemplo, la clave del esquema de wmhtml://, que se usa para transmitir medios enriquecidos, se denomina "wmhtml". Se mantiene una lista independiente para la máquina local y para cada usuario. Para la máquina local, las claves de esquema son subclaves de la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Multimedia \\ WMPlayer \\ Schemes\\**

Por ejemplo, la clave del esquema de wmhtml:// para la máquina local es:

**HKEY \_ LOCAL MACHINE Software Microsoft Multimedia \_ \\ \\ \\ \\ WMPlayer \\ Schemes \\ wmhtml**

Para cambiar los valores de esta clave o para crear una nueva subclave, el usuario actual debe ser administrador del equipo.

Para usuarios individuales, las claves de esquema son subclaves de la siguiente clave del Registro:

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ Schemes\\**

Por ejemplo, la clave del esquema de wmhtml:// para el usuario actual es:

**HKEY \_ CURRENT USER Software Microsoft \_ \\ \\ \\ MediaPlayer Player \\ \\ Schemes \\ wmhtml**

Al comprobar los esquemas registrados, el reproductor comprueba primero los valores ubicados en **HKEY \_ LOCAL \_ MACHINE**. Si no se encuentra ninguno para el esquema actual, el reproductor comprueba los valores en **HKEY \_ CURRENT \_ USER**. Si no se encuentra ninguno para el esquema actual, el reproductor muestra la advertencia al usuario.

Cada subclave de esquema puede contener uno de los siguientes valores posibles *para* runtime.



| Value | Descripción                                |
|-------|--------------------------------------------|
| 6     | Represente mediante el SDK Windows Media Format. |
| 7     | Representar mediante Microsoft DirectShow.         |



 

Cambiar el *valor en* tiempo de ejecución de un esquema que Windows SDK de formato multimedia no tendrá ningún efecto. El reproductor siempre usará el SDK Windows Media Format como tiempo de ejecución para los esquemas que admite Windows SDK de formato multimedia. Este valor del Registro está diseñado para permitir la configuración en tiempo de ejecución para esquemas personalizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del Registro**](registry-settings.md)
</dt> </dl>

 

 




