---
title: Nombre de archivo Extensión del Registro Configuración
description: Nombre de archivo Extensión del Registro Configuración
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Reproductor de Windows Media,registry
- Reproductor de Windows Media,extensiones de nombre de archivo
- registry,file name extensions
- registry,settings for Reproductor de Windows Media
- configuración del Registro de extensiones de nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241773"
---
# <a name="file-name-extension-registry-settings"></a>Nombre de archivo Extensión del Registro Configuración

Si los archivos multimedia digitales tienen un formato personalizado, puede proporcionar a Reproductor de Windows Media información sobre el formato personalizado colocando entradas en el Registro en el equipo del usuario. Reproductor de Windows Media inspecciona las entradas del Registro para determinar cómo debe controlar los archivos. En la lista siguiente se muestran varias de las cosas que puede hacer mediante la creación de entradas del Registro que pertenecen al formato de archivo multimedia personalizado.

-   Conceda permiso al reproductor para reproducir, copiar o transcodificar los archivos.
-   Especifique la tecnología subyacente que el reproductor debe usar para reproducir los archivos.
-   Especifique dónde debe mostrar el reproductor los archivos en su vista de biblioteca.
-   Especifique un complemento que el reproductor debe usar para convertir los archivos a un formato estándar.
-   Especifique un código de formato MTP (Media Transport Protocol) que el reproductor pueda usar para determinar si un dispositivo portátil determinado admite el formato de archivo.

La mayoría de las entradas que proporcione estarán bajo una subclave asociada a la extensión de nombre de archivo personalizada. Puede crear esa subclave en el subárbol HKEY LOCAL MACHINE y en \_ \_ el subárbol HKEY \_ CURRENT \_ USER. Reproductor de Windows Media busca primero en el subárbol HKEY \_ LOCAL \_ MACHINE. Si no encuentra lo que necesita allí, busca en el subárbol HKEY \_ CURRENT \_ USER. Tenga en cuenta que cualquier código que intente escribir en el Registro en el equipo del usuario solo puede escribir en el subárbol HKEY LOCAL MACHINE si el usuario actual tiene \_ \_ privilegios administrativos.

Para escribir información sobre el formato de archivo personalizado en el subárbol HKEY \_ LOCAL \_ MACHINE, cree la subclave siguiente.

**HKEY \_ LOCAL \_ MACHINE Software Microsoft Multimedia \\ \\ \\ \\ WMPlayer \\ Extensions \\** *customExtension*

donde *customExtension* es la extensión de nombre de archivo, incluido el separador de puntos (.). Por ejemplo, si la extensión del formato de archivo personalizado es .xyz, cree la subclave siguiente.

**HKEY \_ LOCAL MACHINE Software Microsoft Multimedia \_ \\ \\ \\ \\ WMPlayer \\ Extensions \\ .xyz**

Para escribir información sobre el formato de archivo personalizado en el subárbol HKEY \_ CURRENT \_ USER, cree la siguiente subclave.

**HKEY \_ CURRENT \_ USER Software Microsoft \\ \\ \\ MediaPlayer Player \\ \\ Extensions \\** *customExtension*

Puede escribir una o varias de las siguientes entradas en la *subclave customExtension.*

-   **Permisos**
-   **Tiempo de ejecución**
-   **FormatCode**

Para especificar complementos de conversión para el formato de archivo multimedia personalizado, cree una subclave **ConvertPluginCLSID** en la subclave *customExtension.*

Para especificar dónde Reproductor de Windows Media mostrar los archivos en su vista de biblioteca, escriba una entrada que represente el formato de archivo personalizado en la subclave siguiente.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

En los temas siguientes se describen las subclaves y las entradas del Registro que proporcionan Reproductor de Windows Media información sobre los formatos de archivo multimedia personalizados.

-   [Entrada del Registro de permisos](permissions-registry-entry.md)
-   [Entrada del Registro en tiempo de ejecución](runtime-registry-entry.md)
-   [Entrada del Registro FormatCode](formatcode-registry-entry.md)
-   [Entradas del Registro de clasificación de bibliotecas](library-classification-registry-entries.md)
-   [Subclave ConvertPluginCLSID](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del Registro**](registry-settings.md)
</dt> <dt>

[**Reproductor de Windows Media Complementos de conversión**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




