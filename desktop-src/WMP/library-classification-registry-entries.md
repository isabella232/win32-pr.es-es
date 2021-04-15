---
title: Entradas del registro de clasificación de biblioteca
description: Entradas del registro de clasificación de biblioteca
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player, biblioteca
- Windows Media Player, entradas del registro de clasificación
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- registro, entradas de clasificación de biblioteca
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- Biblioteca, entradas del registro de clasificación
- Biblioteca, registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695390"
---
# <a name="library-classification-registry-entries"></a>Entradas del registro de clasificación de biblioteca

Cuando Windows Media Player encuentra un archivo multimedia que tiene una extensión de nombre de archivo personalizada, no sabe si el archivo debe clasificarse como audio, vídeo o algún otro tipo. De forma predeterminada, Windows Media Player coloca dichos archivos en la otra parte multimedia de la biblioteca.

Si los archivos multimedia digitales tienen un formato personalizado, puede proporcionar a Windows Media Player información sobre el lugar en el que los archivos deben aparecer en la biblioteca del reproductor colocando dos entradas en el registro en el equipo del usuario.

Una entrada entra en la subclave siguiente.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ extensions**

La entrada del registro tiene el siguiente formato.



| Nombre                                                  | Tipo de datos   | Value                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| La extensión de nombre de archivo sin el separador de puntos (.) | **Registro \_ SZ** | Cadena que especifica la ubicación de una biblioteca. |



 

La otra entrada del registro entra en la siguiente subclave que cree.

**HKEY \_ Clases \_ raíz \\** *customExtension*

donde *customExtension* es la extensión de nombre de archivo, incluido el separador de puntos (.).

La entrada del registro tiene el siguiente formato.



| Nombre          | Tipo de datos   | Value                                      |
|---------------|-------------|--------------------------------------------|
| PerceivedType | **Registro \_ SZ** | Cadena que especifica la ubicación de una biblioteca. |



 

Ambas entradas del registro deben tener el mismo valor. En la tabla siguiente se proporcionan los valores posibles.



| Value | Descripción                                                                      |
|-------|----------------------------------------------------------------------------------|
| audio | Los archivos que tienen la extensión personalizada aparecen en la parte música de la biblioteca. |
| video | Los archivos que tienen la extensión personalizada aparecen en la parte de vídeo de la biblioteca. |



 

Por ejemplo, las siguientes entradas del registro especifican que los archivos que tienen la extensión de nombre de archivo. XYZ aparecerán en la parte de música de la biblioteca:


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



Tenga en cuenta que cualquier código que intente escribir en el registro en el equipo del usuario puede escribir en el \_ subárbol de la máquina local HKEY \_ solo si el usuario actual tiene privilegios administrativos.

Las entradas del registro de clasificación de bibliotecas son compatibles con las siguientes versiones de Windows Media Player.

-   Windows Media Player 9 series con la revisión 823275
-   Windows Media Player 10 y versiones posteriores

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro de la extensión de nombre de archivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




