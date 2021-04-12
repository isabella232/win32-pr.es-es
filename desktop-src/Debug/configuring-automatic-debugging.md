---
description: Los usuarios pueden configurar la depuración automática para ayudarles a determinar por qué el sistema o una aplicación han dejado de responder.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configuración de la depuración automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152745"
---
# <a name="configuring-automatic-debugging"></a>Configuración de la depuración automática

Los usuarios pueden configurar la depuración automática para ayudarles a determinar por qué el sistema o una aplicación han dejado de responder.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Configurar la depuración automática para los bloqueos del sistema

Para configurar el equipo de destino para que genere un archivo de volcado cuando el sistema deje de responder, use la aplicación **sistema** en el panel de control. Haga clic en **Configuración avanzada del sistema**, que muestra el cuadro de diálogo **propiedades del sistema** . En la pestaña **Opciones avanzadas** de ese cuadro, haga clic en **configuración** en **Inicio y recuperación** y, a continuación, use las opciones de recuperación adecuadas. Como alternativa, puede configurar las opciones de volcado de memoria con la siguiente clave del registro:

**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local CrashControl

El archivo que se puede especificar es el archivo de volcado de memoria. Su nombre predeterminado es Memory. DMP. Puede depurar un volcado de memoria con un depurador en modo kernel, como WinDbg o KD. Para obtener más información, vea la documentación que se incluye con el depurador.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Configuración de la depuración automática para bloqueos de la aplicación

Cuando una aplicación deja de responder (por ejemplo, después de una infracción de acceso), el sistema invoca automáticamente un depurador que se especifica en el registro para la depuración de postmortem, el identificador de proceso y el identificador de evento se pasan al depurador si la línea de comandos está configurada correctamente. En el procedimiento siguiente se describe cómo especificar un depurador en el registro.

**Para establecer un depurador como el depurador de postmortem**

1.  Vaya a la siguiente clave del registro:

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AEDebug**

2.  Agregue o edite el valor del **depurador** mediante una cadena de reg \_ SZ que especifica la línea de comandos para el depurador.

    La cadena debe incluir la ruta de acceso completa al archivo ejecutable del depurador. Indique el identificador de proceso y el identificador de evento con los parámetros "% LD" en la línea de comandos del depurador. Los depuradores diferentes pueden tener sus propias sintaxis de parámetros para indicar estos valores. Cuando se invoca el depurador, el primer "% LD" se reemplaza por el identificador del proceso y el segundo "% LD" se reemplaza por el identificador del evento.

    El siguiente texto es un ejemplo de cómo configurar WinDbg como el depurador.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Si desea que el depurador se invoque sin interacción del usuario, agregue o edite el valor **auto** mediante una \_ cadena de reg SZ que especifica si el sistema debe mostrar un cuadro de diálogo al usuario antes de que se invoque el depurador. La cadena "1" deshabilita el cuadro de diálogo; la cadena "0" habilita el cuadro de diálogo.

## <a name="excluding-an-application-from-automatic-debugging"></a>Excluir una aplicación de la depuración automática

En el procedimiento siguiente se describe cómo excluir una aplicación de la depuración automática después de que el valor **auto** en la clave **AEDebug** se haya establecido en 1.

**Para excluir una aplicación de la depuración automática**

1.  Vaya a la siguiente clave del registro:

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AEDebug**

2.  Agregue un \_ valor de REG DWORD a la subclave **AutoExclusionList** , donde name es el nombre del archivo ejecutable y el valor es 1. De forma predeterminada, el Administrador de ventanas de escritorio (Dwm.exe) se excluye de la depuración automática porque, de lo contrario, se puede producir un interbloqueo del sistema si Dwm.exe deja de responder (el usuario no puede ver la interfaz que muestra el depurador porque Dwm.exe no responde y Dwm.exe no puede finalizar porque está retenida por el depurador).

    **Windows Server 2003 y Windows XP:** La subclave **AutoExclusionList** no está disponible; por lo tanto, no puede excluir ninguna aplicación, incluido Dwm.exe, de la depuración automática.

Las entradas del registro de **AEDebug** predeterminadas se pueden representar de la siguiente manera:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar la depuración de postmortem con WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
