---
description: Las aplicaciones, los procesos y las ventanas pueden optar por dejar de estar disponibles para el anclaje en la barra de tareas o para su inclusión en la lista de uso más frecuente (MFU) del menú Inicio.
title: Cómo excluir elementos del anclaje de la barra de tareas y listas recientes/frecuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985442"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Cómo excluir elementos del anclaje de la barra de tareas y listas recientes/frecuentes

Las aplicaciones, los procesos y las ventanas pueden optar por dejar de estar disponibles para el anclaje en la barra de tareas o para su inclusión en la lista de uso más frecuente (MFU) del menú **Inicio** .

## <a name="instructions"></a>Instrucciones


Existen tres mecanismos para conseguir la exclusión de elementos del anclaje de la barra de tareas y listas recientes/frecuentes:

-   Agregue la entrada NoStartPage al registro de la aplicación como se muestra en este ejemplo:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Se omiten los datos asociados a la entrada NoStartPage. Solo se requiere la presencia de la entrada. Por lo tanto, el tipo ideal para NoStartPage es **reg \_ None**.

    Tenga en cuenta que cualquier uso de un identificador de modelo de usuario de aplicación explícito (AppUserModelID) reemplaza la entrada NoStartPage. Si se aplica un AppUserModelID explícito a un acceso directo, proceso o ventana, se convierte en anclable y es válido para la lista de MFU del menú **Inicio** .

-   Establezca la propiedad [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) en Windows y los métodos abreviados. Esta propiedad se debe establecer en una ventana antes de que se establezca la propiedad [PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) .
-   Agregue un AppUserModelID explícito como valor en la subclave del Registro siguiente, tal como se muestra en este ejemplo:

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

    Cada entrada es un valor de **reg \_ null** con el nombre de AppUserModelID. Cualquier AppUserModelID que se encuentre en esta lista no es anclable y no es válido para su inclusión en la lista de MFU del menú **Inicio** .

## <a name="remarks"></a>Observaciones

Tenga en cuenta que determinados archivos ejecutables, así como accesos directos que contienen determinadas cadenas en sus nombres, se excluyen automáticamente del anclaje y la inclusión en la lista de MFU.

> [!Note]  
> Esta exclusión automática se puede invalidar mediante la aplicación de un AppUserModelID explícito.

 

Si alguna de las siguientes cadenas, con independencia del caso, se incluye en el nombre de acceso directo, el programa no se muestra anclado y no se muestra en la lista de elementos usados con mayor frecuencia (no aplicable a Windows 10):

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
-   Novedades

La siguiente lista de programas no es anclable y se excluyen de la lista de uso más frecuente:

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

Las listas anteriores se almacenan en los siguientes valores del registro.

> [!Note]  
> Las aplicaciones no deben modificar estas listas. Use uno de los métodos de lista de exclusión descritos anteriormente en este tema para obtener la misma experiencia.

 

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

[La barra de tareas](taskbar.md)
</dt> <dt>

[Extensiones de la barra de tareas](taskbar-extensions.md)
</dt> </dl>

 

 
