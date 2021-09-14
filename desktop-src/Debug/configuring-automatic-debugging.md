---
description: Los usuarios pueden configurar la depuración automática para ayudarles a determinar por qué su sistema o una aplicación han dejado de responder.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configuración de la depuración automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164669"
---
# <a name="configuring-automatic-debugging"></a>Configuración de la depuración automática

Los usuarios pueden configurar la depuración automática para ayudarles a determinar por qué su sistema o una aplicación han dejado de responder.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Configuración de la depuración automática para bloqueos del sistema

Para configurar el equipo de destino para generar un archivo  de volcado de memoria cuando el sistema deje de responder, use la aplicación Sistema en Panel de control. Haga **clic en Configuración avanzada del** sistema , que muestra el cuadro de diálogo **Propiedades** del sistema . En la **pestaña Avanzadas** de ese cuadro, haga clic Configuración **en** Inicio y recuperación **y,** a continuación, use las opciones de recuperación adecuadas. Como alternativa, puede configurar las opciones de volcado de memoria mediante la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **CrashControl**

El archivo que puede especificar es el archivo de volcado de memoria. Su nombre predeterminado es Memory.dmp. Puede depurar un volcado de memoria con un depurador en modo kernel, como WinDbg o KD. Para obtener más información, vea la documentación incluida con el depurador.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Configuración de la depuración automática para bloqueos de aplicaciones

Cuando una aplicación deja de responder (por ejemplo, después de una infracción de acceso), el sistema invoca automáticamente un depurador especificado en el Registro para la depuración postmortem, el identificador de proceso y el identificador de eventos se pasan al depurador si la línea de comandos está configurada correctamente. En el procedimiento siguiente se describe cómo especificar un depurador en el Registro.

**Para establecer un depurador como depurador postmortem**

1.  Vaya a la siguiente clave del Registro:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Agregue o edite el **valor del** depurador mediante una cadena REG SZ que especifique la línea de comandos para \_ el depurador.

    La cadena debe incluir la ruta de acceso completa al ejecutable del depurador. Indique el identificador de proceso y el identificador de eventos con parámetros "%ld" en la línea de comandos del depurador. Los distintos depuradores pueden tener sus propias sintaxis de parámetros para indicar estos valores. Cuando se invoca el depurador, el primer "%ld" se reemplaza por el identificador de proceso y el segundo "%ld" se reemplaza por el identificador de evento.

    El texto siguiente es un ejemplo de cómo configurar WinDbg como depurador.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Si desea que el depurador se invoque  sin interacción del usuario, agregue o edite el valor Automático mediante una cadena REG SZ que especifique si el sistema debe mostrar un cuadro de diálogo al usuario antes de invocar el \_ depurador. La cadena "1" deshabilita el cuadro de diálogo; la cadena "0" habilita el cuadro de diálogo.

## <a name="excluding-an-application-from-automatic-debugging"></a>Exclusión de una aplicación de la depuración automática

En el procedimiento siguiente se describe cómo excluir una aplicación de la depuración automática después de que el valor **Auto** de la clave **AeDebug** se haya establecido en 1.

**Para excluir una aplicación de la depuración automática**

1.  Vaya a la siguiente clave del Registro:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Agregue un valor REG DWORD a la \_ subclave **AutoExclusionList,** donde el nombre es el nombre del archivo ejecutable y el valor es 1. De forma predeterminada, el Administrador de ventanas de escritorio (Dwm.exe) se excluye de la depuración automática porque, de lo contrario, se puede producir un interbloqueo del sistema si Dwm.exe deja de responder (el usuario no puede ver la interfaz mostrada por el depurador porque Dwm.exe no responde y Dwm.exe no puede finalizar porque lo mantiene el depurador).

    **Windows Server 2003 y Windows XP:** La **subclave AutoExclusionList** no está disponible; por lo tanto, no se puede excluir ninguna aplicación, Dwm.exe, de la depuración automática.

Las entradas predeterminadas del Registro **AeDebug** se pueden representar de la siguiente manera:

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

[Habilitación de la depuración postmortem con WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
