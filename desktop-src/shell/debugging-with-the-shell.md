---
description: En este tema se explica cómo depurar archivos DLL de extensión de shell y de espacio de nombres.
title: Depuración con el shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 276023e5628ab7390398fd7bd367be32e45c13825fcf96625104be1ded8735de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032833"
---
# <a name="debugging-with-the-shell"></a>Depuración con el shell

En este tema se explica cómo depurar archivos DLL de extensión de shell y de espacio de nombres.

-   [Ejecutar el shell en un depurador](#running-the-shell-under-a-debugger)
-   [Ejecución y prueba de extensiones de Shell](#running-and-testing-shell-extensions)
-   [Descarga del archivo DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Ejecutar el shell en un depurador

Para depurar la extensión, debe ejecutar el shell desde el depurador. Siga estos pasos:

1.  Cargue el proyecto de la extensión en el depurador, pero no lo ejecute.
2.  Apague el shell.

    -   Para Windows Vista y versiones posteriores:
        1.  Muestra el **menú** Inicio.
        2.  Presione CTRL+MAYÚS y haga clic con el botón derecho en el fondo de la mitad derecha del **menú** Inicio.
        3.  En el menú que aparece, elija **Salir del Explorador.**
    -   Para Windows XP:
        1.  En el **menú** Inicio, elija **Apagar.**
        2.  Presione CTRL+ALT+MAYÚS y haga clic **en No** en el cuadro de **diálogo** Windows cierre.

    El shell ahora está apagado, pero todas las demás aplicaciones siguen ejecutándose, incluido el depurador.

3.  Establezca el depurador para ejecutar el archivo DLL de extensión Explorer.exe desde **el Windows** archivo.
4.  Ejecute el proyecto desde el depurador. El shell se iniciará como de costumbre, pero el depurador se adjuntará al proceso del shell.

## <a name="running-and-testing-shell-extensions"></a>Ejecutar y probar extensiones de Shell

Puede ejecutar y probar las extensiones en un proceso independiente Windows Explorer para evitar detener y reiniciar el escritorio y la barra de tareas. El escritorio y la barra de tareas se pueden seguir utilizando mientras se ejecutan y prueban las extensiones.

Para habilitar esta característica, agregue la siguiente entrada REG \_ DWORD al Registro.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Para que esta entrada suba efecto, debe cerrar la sesión y volver a iniciarla. Esta configuración hace que las ventanas de escritorio y de barra de tareas se cree en un proceso de Explorer.exe y todas las demás ventanas de explorador y carpeta se abran en un proceso Explorer.exe tareas.

Además de hacer que la ejecución y prueba de las extensiones sea más cómoda, esta configuración también hace que el escritorio sea más sólido en lo que se refiere a las extensiones de Shell. Muchas de estas extensiones (por ejemplo, las extensiones del menú contextual) se cargarán en el proceso de Explorer.exe de entrega. Si finaliza este proceso, el escritorio y la barra de tareas no se verán afectados y la siguiente ventana del Explorador o carpeta volverá a crear el proceso finalizado.

## <a name="unloading-the-dll"></a>Descarga del archivo DLL

El shell descarga automáticamente cualquier archivo DLL cuando su recuento de uso es cero, pero solo después de que el archivo DLL no se haya usado durante un período de tiempo. Este período inactivo puede ser inaceptablemente largo en ocasiones, especialmente cuando se depura un archivo DLL de extensión de Shell. Puede acortar el período inactivo agregando la siguiente información al Registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



