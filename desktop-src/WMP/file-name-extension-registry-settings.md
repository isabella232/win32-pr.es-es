---
title: Configuración del registro de la extensión de nombre de archivo
description: Configuración del registro de la extensión de nombre de archivo
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Media Player de Windows, registro
- Windows Media Player, extensiones de nombre de archivo
- registro, extensiones de nombre de archivo
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778487"
---
# <a name="file-name-extension-registry-settings"></a>Configuración del registro de la extensión de nombre de archivo

Si los archivos multimedia digitales tienen un formato personalizado, puede proporcionar a Windows Media Player información acerca del formato personalizado colocando entradas en el registro en el equipo del usuario. Windows Media Player inspecciona las entradas del registro para determinar cómo debe controlar los archivos. La lista siguiente muestra algunas de las cosas que puede hacer mediante la creación de entradas del registro que pertenecen a su formato de archivo multimedia personalizado.

-   Conceda permiso al reproductor para reproducir, copiar o transcodificar los archivos.
-   Especifique la tecnología subyacente que el reproductor debe usar para reproducir los archivos.
-   Especifique dónde debe mostrar los archivos el reproductor en la vista biblioteca.
-   Especifique un complemento que el reproductor debe usar para convertir los archivos a un formato estándar.
-   Especifique un código de formato MTP (Protocolo de transporte de medios) que el reproductor pueda utilizar para determinar si un dispositivo portátil determinado es compatible con el formato de archivo.

La mayoría de las entradas que proporcione estarán en una subclave asociada a la extensión de nombre de archivo personalizada. Puede crear esa subclave en el \_ \_ subárbol del equipo local HKEY y en el \_ subárbol de usuario de HKEY current \_ . Windows Media Player busca en primer lugar en \_ el \_ subárbol HKEY local Machine. Si no encuentra lo que necesita allí, busca en el \_ subárbol HKEY current \_ User. Tenga en cuenta que cualquier código que intente escribir en el registro en el equipo del usuario puede escribir en el \_ subárbol de la máquina local HKEY \_ solo si el usuario actual tiene privilegios administrativos.

Para escribir información sobre el formato de archivo personalizado en el \_ \_ subárbol HKEY local Machine, cree la siguiente subclave.

**HKEY \_ \_Software de equipo local \\ \\ Microsoft \\ multimedia \\ WMPlayer \\ extensions \\** *customExtension*

donde *customExtension* es la extensión de nombre de archivo, incluido el separador de puntos (.). Por ejemplo, si la extensión del formato de archivo personalizado es. XYZ, cree la subclave siguiente.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimedia \\ WMPlayer \\ extensions \\ . XYZ**

Para escribir información sobre el formato de archivo personalizado en el \_ \_ subárbol HKEY current user, cree la siguiente subclave.

**HKEY \_ \_Software de usuario actual \\ \\ Microsoft \\ MediaPlayer \\ Player \\ extensions \\** *customExtension*

Puede escribir una o varias de las entradas siguientes en la subclave *customExtension* .

-   **Permisos**
-   **Tiempo de ejecución**
-   **FormatCode**

Para especificar los complementos de conversión para el formato de archivo multimedia personalizado, cree una subclave **ConvertPluginCLSID** en la subclave *customExtension* .

Para especificar dónde debe mostrar Windows Media Player los archivos en la vista biblioteca, escriba una entrada que represente el formato de archivo personalizado en la subclave siguiente.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ extensions**

En los temas siguientes se describen las subclaves del registro y las entradas que proporcionan a Windows Media Player información sobre los formatos de archivo multimedia personalizados.

-   [Entrada del registro de permisos](permissions-registry-entry.md)
-   [Entrada del registro en tiempo de ejecución](runtime-registry-entry.md)
-   [Entrada del registro FormatCode](formatcode-registry-entry.md)
-   [Entradas del registro de clasificación de biblioteca](library-classification-registry-entries.md)
-   [Subclave ConvertPluginCLSID](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro**](registry-settings.md)
</dt> <dt>

[**Complementos de conversión de Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




