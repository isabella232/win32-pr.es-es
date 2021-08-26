---
title: La consola de AccChecker
description: AccChecker Console (AccCheckConsole.exe) es una herramienta de línea de comandos para comprobar la implementación de accesibilidad de la interfaz de usuario de la aplicación.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Consola de AccChecker
- Herramienta de línea de comandos AccChecker
- línea de comandos, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272447e2513f109206af6fedaaf6adffe665e8b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887036"
---
# <a name="the-accchecker-console"></a>La consola de AccChecker

AccChecker Console (AccCheckConsole.exe) es una herramienta de línea de comandos para comprobar la implementación de accesibilidad de la interfaz de usuario de la aplicación. La línea de comandos acepta una variedad de entradas (como HWND, el título de la ventana y la rutina de comprobación) y proporciona un código de salida que se corresponde con el recuento de registros de errores.

-   [Sintaxis de la línea de comandos](#command-line-syntax)
-   [Códigos de error de la línea de comandos](#command-line-error-codes)
-   [Ejemplos de línea de comandos](#command-line-examples)
-   [Temas relacionados](#related-topics)

![Herramienta de línea de comandos de la consola de accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Sintaxis de línea de comandos

La consola de AccChecker tiene la siguiente sintaxis de línea de comandos.

**AccCheckConsole \[ options \] (-hwnd &lt; hwnd &gt; \| -process &lt; name ) &gt; \[ &lt; dlls&gt;\]**

Las opciones de línea de comandos son las siguientes.



| Opciones                                                                                                                                                         | Descripción                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd &lt; hwnd&gt;<br/>                                                                     | Valida la ventana que tiene el identificador especificado (HWND). El identificador se puede especificar en hexadecimal o decimal.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window &lt; title&gt;<br/>                                                            | Valida la ventana que tiene el título especificado.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process &lt; name&gt;<br/>                       | Valida la ventana principal del proceso que tiene el nombre especificado.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list<br/>                                       | Enumera todas las rutinas de comprobación disponibles.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable &lt; name&gt;<br/>                          | Ejecuta la rutina de comprobación especificada. Esta opción se puede especificar más de una vez.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable &lt; name&gt;<br/> | Ejecuta todos menos la rutina de comprobación especificada. Esta opción se puede especificar más de una vez.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| warn \| err)<br/>                          | La clasificación de eventos más baja que se registrará.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile &lt; file&gt;<br/>                       | Escriba la salida en el archivo de registro especificado. Esta opción se puede especificar más de una vez.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress &lt; file&gt;<br/>                                                         | Use el archivo XML especificado para suprimir errores. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-quiet<br/>                                                                                             | No escriba la salida del registro en stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help <br/>                           | Muestra ayuda rápida. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Códigos de error de la línea de comandos

A continuación se encuentran los códigos de error devueltos desde AccCheckConsole cuando se usa "echo %errorlevel%"



| Código de error                       | Descripción                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Sin errores ni advertencias.<br/>       |
| <span id="1"></span>1<br/> | Se solicitó la instrucción Usages. <br/> |
| <span id="2"></span>2<br/> | Errores y ninguna advertencia.<br/>          |
| <span id="3"></span>3<br/> | Errores y advertencias.<br/>             |
| <span id="4"></span>4<br/> | Advertencias, pero sin errores.<br/>          |
| <span id="5"></span>5<br/> | Línea de comandos no válida. <br/>           |



 

## <a name="command-line-examples"></a>Ejemplos de línea de comandos

A continuación se muestran varios ejemplos de línea de comandos de la consola de AccChecker.

-   Ejecute todas las comprobaciones en una ventana con un nombre especificado.

    **AccCheckConsole -window "Untitled - Bloc de notas"**

-   Ejecute un subconjunto de las comprobaciones en un HWND y especifique un archivo de supresión.

    **AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**

-   Ejecute todas las comprobaciones desde un nuevo archivo DLL de verificación.

    **AccCheckConsole -window "Untitled - Bloc de notas" VerificationRoutine1.dll**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





