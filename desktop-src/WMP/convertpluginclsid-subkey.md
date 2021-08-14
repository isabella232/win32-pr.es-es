---
title: Subclave ConvertPluginCLSID
description: Subclave ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Reproductor de Windows Media,ConvertPluginCLSID subclave
- Reproductor de Windows Media,extensiones de nombre de archivo
- Reproductor de Windows Media,registry
- registry,file name extensions
- registry,ConvertPluginCLSID subclave
- registry,settings for Reproductor de Windows Media
- configuración del Registro de extensión de nombre de archivo
- Subclave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5deeda3e7eb0b5fe465152aa7711717d086c94a06ebed4f9549dc9f6a9b62dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341669"
---
# <a name="convertpluginclsid-subkey"></a>Subclave ConvertPluginCLSID

Cuando Reproductor de Windows Media 11 encuentra una extensión de nombre de archivo personalizada, busca una subclave del Registro que coincida con la extensión. La subclave se describe en [File Name Extension Registry Configuración](file-name-extension-registry-settings.md). En algunos casos, la subclave de la extensión tiene una subclave denominada **ConvertPluginCLSID.**

Por ejemplo, supongamos que ha creado un formato de archivo personalizado (con la extensión de nombre de archivo .xyz) y un complemento de conversión que convierte los archivos en un formato compatible con Reproductor de Windows Media A continuación, almacenaría el identificador de clase del complemento en una o las dos subclaves siguientes.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Multimedia \\ WMPlayer \\ Extensions \\ .xyz \\ ConvertPluginCLSID**

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ .xyz \\ ConvertPluginCLSID**

La subclave **ConvertPluginCLSID** especifica los id. de clase de los complementos que Reproductor de Windows Media puede usar para convertir un archivo multimedia de su formato personalizado a un formato compatible con el Reproductor.

La **subclave ConvertPluginCLSID** tiene las siguientes entradas.

-   Entrada predeterminada que representa el complemento de conversión predeterminado.
-   Entrada con nombre que representa el complemento de conversión predeterminado.
-   Entradas con nombre adicionales que representan complementos de conversión alternativos.

Por ejemplo, suponga que un formato de archivo personalizado tiene un complemento de conversión predeterminado y dos complementos de conversión alternativos. Las entradas del Registro bajo la subclave **ConvertPluginCLSID** tendrían el formato siguiente.



| Nombre                                                                          | Tipo        | Value                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Valor predeterminado                                                                       | **REG \_ SZ** | Identificador de clase, en formato del Registro, del complemento de conversión predeterminado. |
| Identificador de clase, en formato del Registro, del complemento de conversión predeterminado.          | **REG \_ SZ** | Nombre descriptivo del complemento de conversión predeterminado.                 |
| Identificador de clase, en formato del Registro, del primer complemento de conversión alternativo.  | **REG \_ SZ** | Nombre descriptivo del primer complemento de conversión alternativo.         |
| Identificador de clase, en formato del Registro, del segundo complemento de conversión alternativo. | **REG \_ SZ** | Nombre descriptivo del segundo complemento de conversión alternativo.        |



 

Tenga en cuenta que el complemento de conversión predeterminado se representa mediante dos entradas del Registro: la entrada predeterminada y una entrada con nombre. Reproductor de Windows Media usa la entrada predeterminada para determinar qué complemento es el complemento de conversión predeterminado (principal). Reproductor de Windows Media usa las entradas con nombre para obtener nombres descriptivos para todos los complementos de conversión, incluido el complemento predeterminado.

El nombre descriptivo de un complemento de conversión lo determina la empresa que crea el complemento. Reproductor de Windows Media puede mostrar el nombre descriptivo en su interfaz de usuario.

Cuando Reproductor de Windows Media convertir un archivo de un formato personalizado a un formato estándar, primero carga el complemento predeterminado. Si el complemento predeterminado no puede convertir el archivo y devuelve NS \_ E \_ WMP CONVERT PLUGIN UNKNOWN FILE OWNER, el reproductor carga cada complemento alternativo hasta que se produce una conversión correcta o no hay más complementos que \_ \_ \_ \_ \_ probar. El reproductor no muestra un mensaje de advertencia si no se encuentra ningún complemento de conversión para la extensión de nombre de archivo.

La entrada del Registro **ConvertPluginCLSID** es compatible con Reproductor de Windows Media 11.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensión del Registro de nombre de archivo Configuración**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Reproductor de Windows Media Complementos de conversión**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




