---
title: Redistribuir Reproductor de Windows Media serie 9
description: Redistribuir Reproductor de Windows Media serie 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465521"
---
# <a name="redistributing-windows-media-player-9-series"></a>Redistribuir Reproductor de Windows Media serie 9

Puede instalar Reproductor de Windows Media serie 9 en Windows XP mediante uno de los siguientes programas de instalación.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe es un superconjunto del programa de MPSetupXP.exe programa de instalación. Contiene archivos que son necesarios para los sistemas operativos publicados antes Windows XP. MPSetup.exe es funcionalmente equivalente a MPSetupXP.exe cuando se ejecuta en Windows XP, pero el tamaño del archivo del programa de instalación es mayor porque no se ha optimizado para la instalación en Windows XP.

 

Puede instalar Reproductor de Windows Media serie 9 en Windows 98 Second Edition, Windows Millennium Edition o Windows 2000 mediante el siguiente programa de instalación.

-   MPSetup.exe

Este es un ejemplo de una línea de comandos para la instalación sin interfaz de usuario y sin símbolo del sistema de reinicio o reinicio.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> El parámetro /P: e especifica que el paquete de instalación Reproductor de Windows Media se debe almacenar en caché durante \# Reproductor de Windows Media instalación. Este comando se usa para controlar futuras actualizaciones del sistema operativo. Este comando solo debe omitirlo los administradores de TI corporativos. El único caso en el que /P: e no debe incluirse en la línea de comandos es cuando posee el sistema de destino y sabe que el sistema de destino nunca se actualizará a un \# sistema operativo posterior. Por ejemplo, si va Reproductor de Windows Media instalar la serie 9 en Windows 2000 y el equipo puede actualizarse a Windows XP, debe usar /P: e en la línea de \# comandos. De lo contrario, después Windows la instalación de XP, los archivos Reproductor de Windows Media se sobrescribirán con los archivos de Reproductor de Windows Media para Windows XP.

 

En la tabla siguiente se muestran parámetros adicionales que puede usar con Reproductor de Windows Media programa de instalación de la serie 9.



| Parámetro              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Evitar la migración de bibliotecas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Cree un punto de restauración del sistema anidado. Úsenos si la aplicación crea un punto de restauración del sistema para anidar el Reproductor de Windows Media de restauración dentro del punto de restauración de la aplicación.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | No permitir la creación de un punto de restauración del sistema. Esta marca deshabilitará la creación de un punto de restauración del sistema. En la mayoría de las circunstancias, esta marca no debe usarse para la redistribución general de software. Esto solo se debe usar cuando se puede realizar una elección explícita en nombre del usuario final para no admitir la reversión de los archivos Reproductor de Windows Media a una versión anterior del Reproductor. Esta marca solo debe usarse para la implementación corporativa o la instalación del fabricante de equipos originales (OEM). |



 

## <a name="notes"></a>Notas

-   Los parámetros de la línea de comandos distinguen mayúsculas de minúsculas.
-   Al suprimir el símbolo del sistema de reinicio, debe comprobar la clave del Registro InstallResult y controlar la notificación de reinicio en la aplicación de instalación de llamada.
-   Reproductor de Windows Media serie 9 también instala el runtime de formato multimedia de Windows, por lo que no es necesario incluir el paquete de distribución de Reproductor de Windows Media y el paquete de distribución en tiempo de ejecución de formato multimedia de Windows en el mismo paquete de redistribución de software. Por lo tanto, si incluye MPSetup.exe o MPSetupXP.exe en la instalación, no es necesario incluir WMFdist.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribuir Reproductor de Windows Media Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




