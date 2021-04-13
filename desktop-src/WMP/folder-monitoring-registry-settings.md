---
title: Configuración del registro de supervisión de carpetas
description: Configuración del registro de supervisión de carpetas
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player, configuración del registro de supervisión de carpetas
- Windows Media Player, configuración del registro de supervisión de carpetas de archivos
- Media Player de Windows, registro
- registro, configuración de supervisión de carpetas
- configuración de supervisión de carpeta de archivos, registro
- registro, configuración para Windows Media Player
- configuración del registro de supervisión de carpetas
- configuración del registro de supervisión de carpeta de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421526"
---
# <a name="folder-monitoring-registry-settings"></a>Configuración del registro de supervisión de carpetas

Windows Media Player 9 series o posterior pueden supervisar las carpetas de archivos para los nuevos archivos multimedia digitales. Cuando el reproductor detecta un nuevo archivo en una carpeta supervisada, agrega automáticamente el archivo a la biblioteca. En el caso de Windows Media Player 9 a Windows Media Player 11, los usuarios pueden cambiar la lista de carpetas supervisadas haciendo clic en **supervisar carpetas** en la pestaña biblioteca del cuadro de diálogo **Opciones** . En Windows Media Player 12, un usuario puede cambiar la lista de carpetas supervisadas siguiendo las instrucciones del tema [Agregar elementos a la biblioteca de Windows Media Player](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library). En Windows Media Player 9 a Windows Media Player 11, puede agregar mediante programación una carpeta para su supervisión agregando un valor al registro. En Windows Media Player 12, no puede usar el registro para agregar o quitar mediante programación las carpetas que se van a supervisar.

En Windows Media Player 9 a Windows Media Player 11, para agregar una carpeta que se va a supervisar, primero debe crear o modificar dos valores en la siguiente clave del registro:

**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Preferences\\**

Los valores nuevos deben tener el nombre siguiente.



| Nombre                           | Tipo           | Descripción                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **\_valor DWORD reg** | Valor **DWORD** que representa el recuento de carpetas que se van a supervisar. Debe coincidir con el número de valores **TrackFoldersDirectories ** * * X.                                                                                                                                         |
| **TrackFoldersDirectories * * * X* | **Registro \_ SZ**    | Valor de cadena que representa la ruta de acceso de la carpeta que se va a supervisar. Cada carpeta que se va a supervisar requiere un valor independiente. El sufijo *X* es un entero que siempre debe comenzar en 0 y, a continuación, incrementar en 1. Windows Media Player también supervisa las subcarpetas de la carpeta especificada. |



 

Por ejemplo, para agregar la primera carpeta que se va a supervisar, agregue el valor siguiente:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



A continuación, cree el valor de recuento:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Para agregar una segunda carpeta para supervisar, agregue el valor siguiente:


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

[**Configuración del registro**](registry-settings.md)
</dt> </dl>

 

 




