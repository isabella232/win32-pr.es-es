---
description: El consumidor estándar que implementa la clase ActiveScriptEventConsumer permite que un equipo ejecute un script y tome medidas cuando se produzcan eventos importantes para asegurarse de que un equipo pueda detectar y resolver problemas automáticamente.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Ejecución de un script basado en un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b5950ae8a4e7260932fd4df559a73f3abea2bfaf7722444db0b92470649dd312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816743"
---
# <a name="running-a-script-based-on-an-event"></a>Ejecución de un script basado en un evento

El consumidor estándar que implementa la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) permite que un equipo ejecute un script y tome medidas cuando se produzcan eventos importantes para asegurarse de que un equipo pueda detectar y resolver problemas automáticamente.

Este consumidor se carga de forma predeterminada en el espacio **de nombres de \\ suscripción** raíz.

Puede configurar el rendimiento de todas las instancias de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) en un sistema estableciendo los valores de la propiedad **Timeout** o **MaximumScripts** en una única instancia de [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).

El procedimiento básico para usar consumidores estándar es siempre el mismo y se encuentra en Supervisión y respuesta a eventos [con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md) El siguiente procedimiento que se agrega al procedimiento básico es específico de la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) y describe cómo crear un consumidor de eventos que ejecuta un script.

> [!Caution]  
> La [**clase ActiveScriptEventConsumer**](activescripteventconsumer.md) tiene restricciones de seguridad especiales. Un miembro local del grupo Administradores del equipo local debe configurar este consumidor estándar. Si usa una cuenta de dominio para crear la suscripción, la cuenta LocalSystem debe tener los permisos necesarios en el dominio para comprobar que el creador es miembro del grupo de administradores local.

 

En el procedimiento siguiente se describe cómo crear un consumidor de eventos que ejecuta un script.

**Para crear un consumidor de eventos que ejecute un script**

1.  Escriba el script para ejecutarlo cuando se produce un evento.

    Puede escribir el script en cualquier lenguaje, pero asegúrese de que un motor de scripting para el lenguaje que elija esté instalado en el equipo. El script no tiene que usar objetos de scripting WMI.

    Solo un administrador puede configurar un consumidor de scripts y el script se ejecuta con las credenciales de LocalSystem, lo que proporciona amplias funcionalidades al consumidor, excepto el acceso a la red. Sin embargo, el script no tiene acceso a datos de inicio de sesión de usuario específicos, por ejemplo, variables de entorno y recursos compartidos de red.

2.  En el Managed Object Format (MOF), cree una instancia de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para recibir los eventos que solicite en la consulta.

    Puede colocar el texto del script en **ScriptText** o puede especificar la ruta de acceso y el nombre de archivo del script en **ScriptFileName**. Para obtener más información, vea [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).

3.  Cree una instancia de [**\_ \_ EventFilter,**](--eventfilter.md)así móntela y, a continuación, cree una consulta para especificar el tipo de evento, lo que desencadena la ejecución del script.

    Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md)

4.  Cree una instancia de [**\_ \_ FilterToConsumerBinding para**](--filtertoconsumerbinding.md) asociar el filtro a la instancia de [**ActiveScriptEventConsumer.**](activescripteventconsumer.md)
5.  Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).

En los ejemplos de la sección siguiente se muestran dos maneras de implementar un script controlado por eventos. El primer ejemplo usa un script que se define en un archivo externo y el segundo ejemplo usa un script integrado en el código MOF. Los ejemplos están en código MOF, pero puede crear las instancias mediante programación mediante [scripting API](scripting-api-for-wmi.md) para WMI o la API COM [para WMI.](com-api-for-wmi.md)

## <a name="example-using-an-external-script"></a>Ejemplo de uso de un script externo

En el procedimiento siguiente se describe cómo usar el ejemplo de script externo.

**Para usar el ejemplo de script externo**

1.  Cree un archivo denominado c: \\Asec.vbs y copie el script de este ejemplo en él.
2.  Copie la lista MOF en un archivo de texto y guárdela con una extensión .mof.
3.  En una ventana del símbolo del sistema, compile el archivo MOF con el siguiente comando.

    **Mofcomp** *filename:.mof**

4.  Ejecute la calculadora, que crea un calc.exe proceso. Espere más de cinco segundos, cierre la ventana Calculadora y busque en el directorio C: un archivo \\ denominado ASEC.log.

    El texto siguiente es similar al texto que se incluirá en el archivo ASEC.log.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

En el ejemplo de código de VBScript siguiente se muestra el script al que se llama cuando el consumidor permanente recibe un evento. El **objeto TargetEvent** es una [**\_ \_ instancia de InstanceDeletionEvent,**](--instancedeletionevent.md) por lo que tiene una propiedad denominada **TargetInstance**, que es una instancia de Proceso de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) que se usa para abrir el evento. La **clase Win32 \_ Process** tiene las propiedades **UserModeTime** y **KernelModeTime** que se coloca en el archivo de registro creado por el script.


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



El siguiente ejemplo de código MOF llama al script cuando se recibe un evento. Crea el filtro, el consumidor y el enlace entre ellos en el espacio **de nombres de la \\ suscripción** raíz.

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a>Ejemplo de uso de script en línea

En el procedimiento siguiente se describe cómo usar el ejemplo de script en línea.

**Para usar el ejemplo de script en línea**

1.  Copie la lista MOF de esta sección en un archivo de texto y guárdela con una extensión .mof.
2.  En una ventana del símbolo del sistema, compile el archivo MOF con el siguiente comando.

    **Mofcomp** *filename:.mof**

El siguiente ejemplo de código MOF crea el filtro, el consumidor y el enlace entre ellos y también contiene el script en línea.

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
