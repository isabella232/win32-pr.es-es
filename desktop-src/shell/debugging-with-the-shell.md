---
description: En este tema se explica cómo depurar los archivos dll de extensión de espacio de nombres y Shell.
title: Depuración con el shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540531"
---
# <a name="debugging-with-the-shell"></a>Depuración con el shell

En este tema se explica cómo depurar los archivos dll de extensión de espacio de nombres y Shell.

-   [Ejecutar el Shell en un depurador](#running-the-shell-under-a-debugger)
-   [Ejecutar y probar extensiones de Shell](#running-and-testing-shell-extensions)
-   [Descargar el archivo DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Ejecutar el Shell en un depurador

Para depurar la extensión, debe ejecutar el shell desde el depurador. Siga estos pasos:

1.  Cargue el proyecto de la extensión en el depurador, pero no lo ejecute.
2.  Cierre el shell.

    -   Para Windows Vista y versiones posteriores:
        1.  Mostrar el menú **Inicio** .
        2.  Presione CTRL + MAYÚS y haga clic con el botón secundario en el fondo de la mitad derecha del menú **Inicio** .
        3.  En el menú que aparece, elija **salir del explorador**.
    -   Para Windows XP:
        1.  En el menú **Inicio** , elija **apagar**.
        2.  Presione CTRL + ALT + MAYÚS y haga clic en **no** en el cuadro de diálogo **cerrar Windows** .

    El Shell se ha cerrado, pero todas las demás aplicaciones todavía se están ejecutando, incluido el depurador.

3.  Establezca el depurador para ejecutar el archivo DLL de extensión con Explorer.exe desde el directorio de **Windows** .
4.  Ejecute el proyecto desde el depurador. El Shell se iniciará como de costumbre, pero el depurador se adjuntará al proceso del shell.

## <a name="running-and-testing-shell-extensions"></a>Ejecutar y probar extensiones de Shell

Puede ejecutar y probar las extensiones en un proceso independiente del explorador de Windows para evitar detener y reiniciar el escritorio y la barra de tareas. El escritorio y la barra de tareas se pueden seguir usando mientras ejecuta y prueba las extensiones.

Para habilitar esta característica, agregue la siguiente \_ entrada REG DWORD al registro.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Para que esta entrada surta efecto, debe cerrar la sesión y volver a iniciarla. Esta configuración hace que las ventanas del escritorio y de la barra de tareas se creen en un proceso Explorer.exe y en el resto de las ventanas del explorador y de las carpetas que se van a abrir en otro proceso de Explorer.exe.

Además de hacer que la ejecución y las pruebas de las extensiones sean más cómodas, esta opción también hace que el escritorio sea más sólido en lo relacionado con las extensiones de Shell. Muchas de estas extensiones (por ejemplo, extensiones de menú contextual) se cargarán en el proceso de Explorer.exe de no escritorio. Si finaliza este proceso, el escritorio y la barra de tareas no se verán afectados y la siguiente ventana explorador o carpeta volverá a crear el proceso terminado.

## <a name="unloading-the-dll"></a>Descargar el archivo DLL

El shell descarga automáticamente cualquier archivo DLL cuando su recuento de uso es cero, pero solo después de que el archivo DLL no se haya usado durante un período de tiempo. Este período inactivo puede ser inaceptablemente largo a veces, especialmente cuando se depura un archivo DLL de extensión de Shell. Puede acortar el período inactivo agregando la siguiente información al registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



