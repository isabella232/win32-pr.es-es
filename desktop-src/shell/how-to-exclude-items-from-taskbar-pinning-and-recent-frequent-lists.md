---
description: Las aplicaciones, los procesos y las ventanas pueden optar por dejar de estar disponibles para anclarse a la barra de tareas o para su inclusión en la lista de uso más frecuente (MFU) de menú Inicio.
title: Cómo excluir elementos de la anclación de la barra de tareas y listas recientes o frecuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3adb60353836e436f4327837c30448c7628a435048cc2a41b0464d56341f410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223569"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Cómo excluir elementos de la anclación de la barra de tareas y listas recientes o frecuentes

Las aplicaciones, los procesos y las ventanas pueden optar por dejar de estar  disponibles para anclarse a la barra de tareas o para su inclusión en la lista De uso más frecuente (MFU) del menú Inicio.

## <a name="instructions"></a>Instrucciones


Hay tres mecanismos para lograr la exclusión de elementos de las listas ancladas de la barra de tareas y las listas recientes o frecuentes:

-   Agregue la entrada NoStartPage al registro de la aplicación como se muestra en este ejemplo:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Se omiten los datos asociados a la entrada NoStartPage. Solo se requiere la presencia de la entrada. Por lo tanto, el tipo ideal para NoStartPage es **REG \_ NONE.**

    Tenga en cuenta que cualquier uso de un identificador de modelo de usuario de aplicación explícito (AppUserModelID) invalida la entrada NoStartPage. Si se aplica un AppUserModelID explícito a un acceso directo, proceso o  ventana, se vuelve anclable y apto para la lista MFU del menú Inicio.

-   Establezca la [propiedad System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) en ventanas y accesos directos. Esta propiedad debe establecerse en una ventana antes de establecer la [propiedad \_ AppUserModel \_ ID de PKEY.](../properties/props-system-appusermodel-id.md)
-   Agregue un AppUserModelID explícito como un valor en la subclave del Registro siguiente, como se muestra en este ejemplo:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Cada entrada es un **valor REG \_ NULL** con el nombre de AppUserModelID. Los AppUserModelID que se encuentran en esta lista no se pueden anclar y no se pueden incluir en la **lista** MFU del menú Inicio.

## <a name="remarks"></a>Comentarios

Tenga en cuenta que determinados archivos ejecutables, así como los accesos directos que contienen determinadas cadenas en sus nombres, se excluyen automáticamente de la anclar e incluir en la lista MFU.

> [!Note]  
> Esta exclusión automática se puede invalidar aplicando un AppUserModelID explícito.

 

Si alguna de las cadenas siguientes, independientemente de las mayúsculas y minúsculas, se incluye en el nombre del acceso directo, el programa no se puede anclar y no se muestra en la lista de uso más frecuente (no se aplica a Windows 10):

-   Documentación
-   Ayuda
-   Instalar
-   Más información
-   Léame
-   Leer primero
-   Léame
-   Quitar
-   Configurar
-   Soporte técnico
-   What's New

La siguiente lista de programas no se puede anclar y se excluye de la lista de uso más frecuente:

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Las listas anteriores se almacenan en los siguientes valores del Registro.

> [!Note]  
> Las aplicaciones no deben modificar estas listas. Use uno de los métodos de lista de exclusión descritos anteriormente en este tema para la misma experiencia.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Barra de tareas](taskbar.md)
</dt> <dt>

[Extensiones de la barra de tareas](taskbar-extensions.md)
</dt> </dl>

 

 
