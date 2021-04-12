---
title: Depurar código
description: Depurar código
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Aspectos de Windows Media Player, código de depuración
- máscaras, código de depuración
- depurar código para máscaras
- Máscaras de Windows Media Player, registro
- máscaras, registro
- funcionalidad de registro en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357611"
---
# <a name="debugging-code"></a>Depurar código

A menudo, querrá ver lo que está ocurriendo dentro de la máscara. Puede hacerlo a través de un control de texto o de un archivo de registro.

Puede crear un elemento de **texto** y colocarlo en una parte de la máscara temporalmente. Por ejemplo, podría usar el código siguiente para crear el elemento de **texto** :


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



Después, por ejemplo, si desea ver la posición actual del contenido multimedia digital en Windows Media Player, puede usar código similar al siguiente para mostrar la posición actual en el cuadro de texto.


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a>Para escribir información de depuración en un archivo de registro

Para habilitar o deshabilitar la depuración, cambie el valor de la siguiente clave del registro:

**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**

Al establecer el valor en 1, el registro está habilitado. Al establecer el valor en 0 (el valor predeterminado), el registro está deshabilitado.

Si el registro está habilitado, se colocará un archivo en el equipo del usuario en la misma carpeta que la máscara. El archivo se denominará "*filename* \_ 0 \_log.txt", donde *filename* es el nombre del archivo de máscara. El código de la máscara puede escribir texto en este archivo mediante el *tema*. método **logString** . Esto puede ser útil si desea determinar lo que está ocurriendo dentro del código mientras se está ejecutando. Tenga en cuenta que el archivo de texto se codifica con caracteres Unicode.

Cuando el registro está habilitado y se ha instalado un sistema de desarrollo que proporciona capacidades de depuración (como Microsoft Visual Studio), las excepciones que no se controlan mediante el código de script provocarán que se abra un cuadro de diálogo de advertencia del depurador para cada excepción. Esta es una característica útil para ayudarle a depurar el código de script. Además, puede adjuntar manualmente el proceso de Media Player de Windows al depurador cuando el registro está habilitado.

Este SDK incluye una máscara de ejemplo, denominada "Logging", que muestra la funcionalidad de registro en máscaras. Para obtener más información sobre el uso de los ejemplos, vea [ejemplos](samples.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las máscaras**](about-skins.md)
</dt> </dl>

 

 




