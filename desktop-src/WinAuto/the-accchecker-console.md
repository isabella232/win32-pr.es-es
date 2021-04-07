---
title: La consola de AccChecker
description: La consola de AccChecker (AccCheckConsole.exe) es una herramienta de línea de comandos para comprobar la implementación de accesibilidad de la interfaz de usuario de la aplicación.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Consola de AccChecker
- Herramienta de línea de comandos AccChecker
- línea de comandos, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903180"
---
# <a name="the-accchecker-console"></a>La consola de AccChecker

La consola de AccChecker (AccCheckConsole.exe) es una herramienta de línea de comandos para comprobar la implementación de accesibilidad de la interfaz de usuario de la aplicación. La línea de comandos acepta diversas entradas (como HWND, título de ventana y rutina de comprobación) y proporciona un código de salida que corresponde al número de registros de errores.

-   [Sintaxis de línea de comandos](#command-line-syntax)
-   [Códigos de error de la línea de comandos](#command-line-error-codes)
-   [Ejemplos de línea de comandos](#command-line-examples)
-   [Temas relacionados](#related-topics)

![herramienta de línea de comandos de la consola de accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Sintaxis de línea de comandos

La consola de AccChecker tiene la siguiente sintaxis de línea de comandos.

**\[Opciones \] de AccCheckConsole (-HWND <hwnd> \| -Process <name> )\[<dlls>\]**

Las opciones de línea de comandos son las siguientes.



| Opciones                                                                                                                                                         | Descripción                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd><br/>                                                                     | Valida la ventana que tiene el identificador especificado (HWND). El identificador se puede especificar en valores hexadecimales o decimales.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-Window <title><br/>                                                            | Valida la ventana que tiene el título especificado.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -proceso <name><br/>                       | Valida la ventana principal del proceso que tiene el nombre especificado.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -lista<br/>                                       | Muestra todas las rutinas de comprobación disponibles.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -habilitar <name><br/>                          | Ejecuta la rutina de comprobación especificada. Esta opción se puede especificar más de una vez.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -Disable <name><br/> | Ejecuta todo excepto la rutina de comprobación especificada. Esta opción se puede especificar más de una vez.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (información \| WARN \| Err)<br/>                          | La clasificación de eventos más baja que se registrará.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file><br/>                       | Escriba la salida en el archivo de registro especificado. Esta opción se puede especificar más de una vez.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suprimir <file><br/>                                                         | Use el archivo XML especificado para suprimir los errores. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-Quiet<br/>                                                                                             | No escriba la salida del registro en stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-Help <br/>                           | Muestra la ayuda rápida. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Códigos de error de la línea de comandos

A continuación se muestran los códigos de error devueltos por AccCheckConsole cuando se usa "echo% ERRORLEVEL%"



| Código de error                       | Descripción                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Sin errores ni advertencias.<br/>       |
| <span id="1"></span>1<br/> | Se solicitó la instrucción Usages. <br/> |
| <span id="2"></span>2<br/> | Errores y sin advertencias.<br/>          |
| <span id="3"></span>3<br/> | Errores y advertencias.<br/>             |
| <span id="4"></span>4<br/> | ADVERTENCIAS pero sin errores.<br/>          |
| <span id="5"></span>5<br/> | Línea de comandos no válida. <br/>           |



 

## <a name="command-line-examples"></a>Ejemplos de línea de comandos

A continuación se muestran varios ejemplos de línea de comandos de la consola de AccChecker.

-   Ejecutar todas las comprobaciones en una ventana con un nombre especificado.

    **AccCheckConsole: ventana "sin título: Bloc de notas"**

-   Ejecutar un subconjunto de las comprobaciones con respecto a un HWND, especificando un archivo de supresión.

    **AccCheckConsole-HWND 0x00382f00-enable CheckTabbing-enable CheckName-Suppress suppress.xml**

-   Ejecutar todas las comprobaciones de una nueva DLL de comprobación.

    **AccCheckConsole-Window "Untitled-Notepad" VerificationRoutine1.dll**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





