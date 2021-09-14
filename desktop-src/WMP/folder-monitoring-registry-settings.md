---
title: Supervisión de carpetas Configuración
description: Supervisión de carpetas Configuración
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Reproductor de Windows Media del Registro de supervisión de carpetas
- Reproductor de Windows Media del Registro de supervisión de carpetas de archivos
- Reproductor de Windows Media,registry
- registro, configuración de supervisión de carpetas
- configuración de supervisión del registro y de la carpeta de archivos
- registry,settings for Reproductor de Windows Media
- configuración del Registro de supervisión de carpetas
- Configuración del Registro de supervisión de carpetas de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170578"
---
# <a name="folder-monitoring-registry-settings"></a>Supervisión de carpetas Configuración

Reproductor de Windows Media serie 9 o posterior puede supervisar carpetas de archivos para nuevos archivos multimedia digitales. Cuando el reproductor detecta un nuevo archivo en una carpeta supervisada, agrega automáticamente el archivo a la biblioteca. Para Reproductor de Windows Media 9 a Reproductor de Windows Media 11, los usuarios pueden cambiar la lista de carpetas supervisadas haciendo clic en **Supervisar** carpetas en la pestaña biblioteca del cuadro **de** diálogo Opciones . Para Reproductor de Windows Media 12, un usuario puede cambiar la lista de carpetas supervisadas siguiendo las instrucciones del tema Add [items to the Reproductor de Windows Media Library](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library). Para Reproductor de Windows Media 9 a Reproductor de Windows Media 11, puede agregar mediante programación una carpeta que se supervisará agregando un valor al Registro. Para Reproductor de Windows Media 12, no puede usar el Registro para agregar o quitar carpetas que se supervisarán mediante programación.

Para Reproductor de Windows Media 9 a Reproductor de Windows Media 11, para agregar una carpeta para la supervisión, primero debe crear o modificar dos valores en la siguiente clave del Registro:

**HKEY \_ CURRENT USER Software \_ \\ \\ Preferencias de Microsoft \\ MediaPlayer \\\\**

Los nuevos valores se deben denominar como se muestra a continuación.



| Nombre                           | Tipo           | Descripción                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **REG \_ DWORD** | Valor **DWORD** que representa el recuento de carpetas que se supervisarán. Debe coincidir con el recuento de **valores TrackFoldersDirectories**_X._                                                                                                                                         |
| **TrackFoldersDirectories**_X_ | **REG \_ SZ**    | Valor de cadena que representa la ruta de acceso de la carpeta que se supervisará. Cada carpeta que se supervisará requiere un valor independiente. El sufijo *X* es un entero que siempre debe comenzar en 0 y, a continuación, incrementar en 1. Reproductor de Windows Media también supervisa las subcarpetas de la carpeta especificada. |



 

Por ejemplo, para agregar la primera carpeta que se supervisará, agregue el siguiente valor:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



A continuación, cree el valor de recuento:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Para agregar una segunda carpeta para supervisar, agregue el siguiente valor:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



A continuación, incremente el valor de recuento:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del Registro**](registry-settings.md)
</dt> </dl>

 

 




