---
title: Entradas del Registro de clasificación de bibliotecas
description: Entradas del Registro de clasificación de bibliotecas
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Reproductor de Windows Media,library
- Reproductor de Windows Media, entradas del Registro de clasificación
- Reproductor de Windows Media,extensiones de nombre de archivo
- Reproductor de Windows Media,registry
- registry,file name extensions
- registro, entradas de clasificación de biblioteca
- registry,settings for Reproductor de Windows Media
- configuración del Registro de extensión de nombre de archivo
- biblioteca, entradas del Registro de clasificación
- library,registry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360561"
---
# <a name="library-classification-registry-entries"></a>Entradas del Registro de clasificación de bibliotecas

Cuando Reproductor de Windows Media encuentra un archivo multimedia que tiene una extensión de nombre de archivo personalizada, no sabe si el archivo debe clasificarse como audio, vídeo u otro tipo. De forma predeterminada, Reproductor de Windows Media estos archivos en la parte Otros medios de la biblioteca.

Si los archivos multimedia digitales tienen un formato personalizado, puede proporcionar a Reproductor de Windows Media información sobre dónde deben aparecer los archivos en la biblioteca del Reproductor colocando dos entradas en el Registro en el equipo del usuario.

Una entrada va en la subclave siguiente.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

La entrada del Registro tiene el formato siguiente.



| Nombre                                                  | Tipo de datos   | Value                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| Extensión de nombre de archivo sin el separador de puntos (.) | **REG \_ SZ** | Cadena que especifica una ubicación de biblioteca |



 

La otra entrada del Registro va en la subclave siguiente que se crea.

**HKEY \_ CLASSES \_ \\ ROOT** *customExtension*

donde *customExtension* es la extensión de nombre de archivo, incluido el separador de puntos (.).

La entrada del Registro tiene el formato siguiente.



| Nombre          | Tipo de datos   | Value                                      |
|---------------|-------------|--------------------------------------------|
| PerceivedType | **REG \_ SZ** | Cadena que especifica una ubicación de biblioteca |



 

Ambas entradas del Registro deben tener el mismo valor. Los valores posibles se dan en la tabla siguiente.



| Value | Descripción                                                                      |
|-------|----------------------------------------------------------------------------------|
| audio | Los archivos que tienen la extensión personalizada aparecen en la parte de música de la biblioteca. |
| video | Los archivos que tienen la extensión personalizada aparecen en la parte de vídeo de la biblioteca. |



 

Por ejemplo, las siguientes entradas del Registro especifican que los archivos que tienen la extensión de nombre de archivo .xyz aparecerán en la parte de música de la biblioteca:


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



Tenga en cuenta que cualquier código que intente escribir en el Registro en el equipo del usuario solo puede escribir en el subárbol HKEY LOCAL MACHINE si el usuario actual tiene \_ \_ privilegios administrativos.

Las siguientes versiones de Reproductor de Windows Media admiten las entradas del Registro de clasificación de bibliotecas.

-   Reproductor de Windows Media serie 9 con revisión 823275
-   Reproductor de Windows Media 10 y versiones posteriores

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensión del Registro de nombre de archivo Configuración**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




