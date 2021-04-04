---
title: Redistribuir Windows Media Player serie 9
description: Redistribuir Windows Media Player serie 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076265"
---
# <a name="redistributing-windows-media-player-9-series"></a>Redistribuir Windows Media Player serie 9

Puede instalar Windows Media Player 9 series en Windows XP con uno de los siguientes programas de instalación.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe es un superconjunto del programa de instalación de MPSetupXP.exe. Contiene archivos que son necesarios para los sistemas operativos publicados antes de Windows XP. MPSetup.exe es funcionalmente equivalente a MPSetupXP.exe cuando se ejecuta en Windows XP, pero el tamaño del archivo del programa de instalación es mayor porque no se ha optimizado para la instalación en los sistemas operativos Windows XP.

 

Puede instalar Windows Media Player 9 series en Windows 98 Second Edition, Windows Millennium Edition o Windows 2000 con el siguiente programa de instalación.

-   MPSetup.exe

Este es un ejemplo de una línea de comandos para la instalación sin interfaz de usuario y sin solicitud de reinicio o reinicio.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> El parámetro/P: \# e especifica que el paquete de instalación de windows media Player debe almacenarse en la memoria caché durante el programa de instalación de windows media Player. Este comando se utiliza para controlar las actualizaciones futuras del sistema operativo. Este comando solo lo deben omitir los administradores de TI corporativos. El único caso en el que/P: \# e no debe incluirse en la línea de comandos es cuando es el propietario del sistema de destino y sabe que el sistema de destino nunca se actualizará a un sistema operativo posterior. Por ejemplo, si va a instalar Windows Media Player 9 series en Windows 2000 y el equipo puede actualizarse algún día a Windows XP, debe usar/P: \# e en la línea de comandos. De lo contrario, después de la instalación de Windows XP, los archivos de Windows Media Player se sobrescribirán con los archivos de Windows Media Player para Windows XP.

 

En la tabla siguiente se muestran parámetros adicionales que puede usar con el programa de instalación de Windows Media Player 9 series.



| Parámetro              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedir la migración de la biblioteca.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Cree un punto de restauración del sistema anidado. Úselo si la aplicación crea un punto de restauración del sistema para anidar el punto de restauración de Windows Media Player en el punto de restauración de la aplicación.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | No permitir la creación de un punto de restauración del sistema. Esta marca deshabilitará la creación de un punto de restauración del sistema. En la mayoría de los casos, esta marca no debe usarse para la redistribución de software general. Esto solo debe usarse cuando se puede realizar una elección explícita en nombre del usuario final para no admitir la reversión de los archivos de Windows Media Player a una versión anterior del reproductor. Esta marca solo se debe usar para la instalación corporativa o la instalación del fabricante de equipos originales (OEM). |



 

## <a name="notes"></a>Notas

-   Los parámetros de la línea de comandos distinguen mayúsculas de minúsculas.
-   Al suprimir el mensaje de reinicio, debe comprobar la clave del registro InstallResult y controlar la notificación de reinicio en la aplicación de instalación que realiza la llamada.
-   Windows Media Player 9 series también instala Windows Media Format en tiempo de ejecución, por lo que no es necesario incluir el paquete de distribución de Windows Media Player y el paquete de distribución en tiempo de ejecución de Windows Media Format en el mismo paquete de distribución de software. Por lo tanto, si incluye MPSetup.exe o MPSetupXP.exe en su instalación, no es necesario incluir WMFdist.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribuir el software de Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




