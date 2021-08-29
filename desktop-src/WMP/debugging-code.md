---
title: Depurar código
description: Depurar código
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Reproductor de Windows Media máscaras,código de depuración
- máscaras, código de depuración
- depuración de código para máscaras
- Reproductor de Windows Media máscaras, registro
- máscaras, registro
- funcionalidad de registro en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d0d8be81c22d06c5d25fa5a3fd33dc17080f0f7851fdfbcb656a3fd99e0854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863595"
---
# <a name="debugging-code"></a>Depurar código

A menudo querrá ver lo que sucede dentro de la máscara. Puede hacerlo a través de un control de texto o a través de un archivo de registro.

Puede crear un elemento **TEXT** y colocarlo temporalmente en una parte de la máscara. Por ejemplo, podría usar el código siguiente para crear el **elemento TEXT:**


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



A continuación, por ejemplo, si desea ver la posición actual del contenido multimedia digital en Reproductor de Windows Media, podría usar código similar al siguiente para mostrar la posición actual en el cuadro de texto.


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a>Para escribir información de depuración en un archivo de registro

Para habilitar o deshabilitar la depuración, cambie el valor de la siguiente clave del Registro:

**HKEY \_ CURRENT \_ USER \\ SOFTWARE \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**

Al establecer el valor en 1, se habilita el registro. Cuando se establece el valor en 0 (valor predeterminado), el registro está deshabilitado.

Si el registro está habilitado, se colocará un archivo en el equipo del usuario en la misma carpeta que la máscara. El archivo se denominará *"nombre de* \_ archivo 0 \_log.txt", donde *filename* es el nombre del archivo de máscara. El código de la máscara puede escribir texto en este archivo mediante el *tema .* **Método logString.** Esto puede ser útil si desea determinar lo que sucede dentro del código mientras se ejecuta. Tenga en cuenta que el archivo de texto está codificado con caracteres Unicode.

Cuando el registro está habilitado y ha instalado un sistema de desarrollo que proporciona funcionalidades de depuración (como Microsoft Visual Studio), las excepciones que no se controlan mediante el código de script harán que se abra un cuadro de diálogo de advertencia del depurador para cada excepción. Se trata de una característica útil para ayudarle a depurar el código de script. Además, puede adjuntar manualmente el proceso de Reproductor de Windows Media al depurador cuando el registro está habilitado.

Este SDK incluye una máscara de ejemplo, denominada "logging", que muestra la funcionalidad de registro en máscaras. Para obtener más información sobre el uso de los ejemplos, vea [Ejemplos](samples.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las máscaras**](about-skins.md)
</dt> </dl>

 

 




