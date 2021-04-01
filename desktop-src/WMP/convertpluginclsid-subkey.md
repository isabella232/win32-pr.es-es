---
title: Subclave ConvertPluginCLSID
description: Subclave ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Media Player de Windows, subclave ConvertPluginCLSID
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- Registry, subclave ConvertPluginCLSID
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- Subclave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075815"
---
# <a name="convertpluginclsid-subkey"></a>Subclave ConvertPluginCLSID

Cuando Windows Media Player 11 encuentra una extensión de nombre de archivo personalizada, busca una subclave del registro que coincida con la extensión. La subclave se describe en [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo. En algunos casos, la subclave de la extensión tiene una subclave denominada **ConvertPluginCLSID**.

Por ejemplo, supongamos que ha creado un formato de archivo personalizado (con la extensión de nombre de archivo. XYZ) y un complemento de conversión que convierte los archivos a un formato compatible con Windows Media Player, a continuación, almacenaría el ID. de clase del complemento en una o las dos subclaves siguientes.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimedia \\ WMPlayer \\ extensions \\ . XYZ \\ ConvertPluginCLSID**

**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ extensions \\ . XYZ \\ ConvertPluginCLSID**

La subclave **ConvertPluginCLSID** especifica los identificadores de clase de los complementos que Windows Media Player puede usar para convertir un archivo multimedia de su formato personalizado a un formato compatible con el reproductor.

La subclave **ConvertPluginCLSID** tiene las siguientes entradas.

-   Entrada predeterminada que representa el complemento de conversión predeterminado.
-   Una entrada con nombre que representa el complemento de conversión predeterminado.
-   Entradas con nombre adicionales que representan complementos de conversión alternativos.

Por ejemplo, supongamos que un formato de archivo personalizado tiene un complemento de conversión predeterminado y dos complementos de conversión alternativos. Las entradas del registro bajo la subclave **ConvertPluginCLSID** tendrían el formato siguiente.



| Nombre                                                                          | Tipo        | Value                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Valor predeterminado                                                                       | **Registro \_ SZ** | IDENTIFICADOR de clase, en formato de registro, del complemento de conversión predeterminado. |
| IDENTIFICADOR de clase, en formato de registro, del complemento de conversión predeterminado.          | **Registro \_ SZ** | Nombre descriptivo del complemento de conversión predeterminado.                 |
| IDENTIFICADOR de clase, en formato de registro, del primer complemento de conversión alternativo.  | **Registro \_ SZ** | Nombre descriptivo del primer complemento de conversión alternativo.         |
| IDENTIFICADOR de clase, en formato de registro, del segundo complemento de conversión alternativo. | **Registro \_ SZ** | Nombre descriptivo del segundo complemento de conversión alternativo.        |



 

Tenga en cuenta que el complemento de conversión predeterminado se representa mediante dos entradas del registro: la entrada predeterminada y una entrada con nombre. Windows Media Player usa la entrada predeterminada para determinar qué complemento es el complemento de conversión predeterminado (principal). Windows Media Player usa las entradas con nombre para obtener nombres descriptivos para todos los complementos de conversión, incluido el complemento predeterminado.

El nombre descriptivo de un complemento de conversión viene determinado por la empresa que crea el complemento. Windows Media Player podría mostrar el nombre descriptivo en su interfaz de usuario.

Cuando Windows Media Player intenta convertir un archivo de un formato personalizado a un formato estándar, carga primero el complemento predeterminado. Si el complemento predeterminado no puede convertir el archivo y devuelve el complemento NS \_ E \_ WMP \_ Convert \_ el \_ \_ archivo desconocido \_ , el reproductor carga cada complemento alternativo hasta que se produce una conversión correcta o no hay más complementos que probar. El reproductor no muestra un mensaje de advertencia si no se encuentra ningún complemento de conversión para la extensión de nombre de archivo.

La entrada del registro **ConvertPluginCLSID** es compatible con Windows Media Player 11.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro de la extensión de nombre de archivo**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Complementos de conversión de Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




