---
description: El consumidor estándar implementado por la clase ActiveScriptEventConsumer permite a un equipo ejecutar un script y tomar medidas cuando se producen eventos importantes para garantizar que un equipo pueda detectar y resolver problemas automáticamente.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Ejecutar un script basado en un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4dbb1e55c7828a79d6541182eff5ce20147a82c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912750"
---
# <a name="running-a-script-based-on-an-event"></a>Ejecutar un script basado en un evento

El consumidor estándar implementado por la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) permite a un equipo ejecutar un script y tomar medidas cuando se producen eventos importantes para garantizar que un equipo pueda detectar y resolver problemas automáticamente.

Este consumidor se carga de forma predeterminada en el espacio de nombres de la **\\ suscripción raíz** .

Puede configurar el rendimiento de todas las instancias de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) en un sistema estableciendo los valores de la propiedad **timeout** o **MaximumScripts** en una única instancia de [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).

El procedimiento básico para usar consumidores estándar siempre es el mismo y se encuentra en [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md). El siguiente procedimiento que agrega al procedimiento básico, es específico de la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) y describe cómo crear un consumidor de eventos que ejecute un script.

> [!Caution]  
> La clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) tiene restricciones de seguridad especiales. Este consumidor estándar debe configurarlo un miembro local del grupo administradores en el equipo local. Si utiliza una cuenta de dominio para crear la suscripción, la cuenta LocalSystem debe tener los permisos necesarios en el dominio para comprobar que el creador es miembro del grupo de administradores locales.

 

En el procedimiento siguiente se describe cómo crear un consumidor de eventos que ejecute un script.

**Para crear un consumidor de eventos que ejecute un script**

1.  Escribir el script para que se ejecute cuando se produzca un evento.

    Puede escribir el script en cualquier lenguaje, pero asegúrese de que se ha instalado en el equipo un motor de scripting para el idioma que elija. El script no tiene que utilizar objetos de scripting de WMI.

    Solo un administrador puede configurar un consumidor de scripts y el script se ejecuta con las credenciales LocalSystem, lo que proporciona amplias capacidades al consumidor excepto el acceso a la red. Sin embargo, el script no tiene acceso a datos de inicio de sesión de usuario específicos, por ejemplo, variables de entorno y recursos compartidos de red.

2.  En el archivo Managed Object Format (MOF), cree una instancia de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para recibir los eventos que solicita en la consulta.

    Puede colocar el texto del script en **ScriptText**, o puede especificar la ruta de acceso y el nombre de archivo del script en **ScriptFileName**. Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

3.  Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md), asígnele un nombre y, a continuación, cree una consulta para especificar el tipo de evento, que desencadena la ejecución del script.

    Para obtener más información, vea [consultas con WQL](querying-with-wql.md).

4.  Cree una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar el filtro a la instancia de [**ActiveScriptEventConsumer**](activescripteventconsumer.md).
5.  Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).

Los ejemplos de la siguiente sección muestran dos maneras de implementar un script orientado a eventos. En el primer ejemplo se usa un script que se define en un archivo externo y en el segundo ejemplo se usa un script integrado en el código MOF. Los ejemplos se encuentran en código MOF, pero puede crear las instancias mediante programación con la API de [scripting para WMI](scripting-api-for-wmi.md) o la [API com para WMI](com-api-for-wmi.md).

## <a name="example-using-an-external-script"></a>Ejemplo de uso de un script externo

En el procedimiento siguiente se describe cómo usar el ejemplo de script externo.

**Para usar el ejemplo de script externo**

1.  Cree un archivo denominado c: \\Asec.vbs y, a continuación, copie en él el script de este ejemplo.
2.  Copie la lista MOF en un archivo de texto y guárdela con una extensión. mof.
3.  En una ventana del símbolo del sistema, compile el archivo MOF con el siguiente comando.

    Nombre de archivo de **MOFCOMP** ** * *. mof**

4.  Ejecute la calculadora, que crea un proceso de calc.exe. Espere más de cinco segundos, cierre la ventana calculadora y busque en el directorio C: \\ un archivo denominado ASEC. log.

    El texto siguiente es similar al texto que se incluirá en el archivo ASEC. log.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

En el siguiente ejemplo de código de VBScript se muestra el script al que se llama cuando el consumidor permanente recibe un evento. El objeto **TargetEvent** es una instancia de [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) , por lo que tiene una propiedad denominada **TargetInstance**, que es una instancia de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que se usa para desencadenar el evento. La clase de **\_ proceso de Win32** tiene las propiedades **UserModeTime** y **KernelModeTime** que se colocan en el archivo de registro creado por el script.


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



El siguiente ejemplo de código MOF llama al script cuando se recibe un evento. Crea el filtro, el consumidor y el enlace entre ellos en el espacio de nombres de la **\\ suscripción raíz** .

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

## <a name="example-using-inline-script"></a>Ejemplo con el script en línea

En el procedimiento siguiente se describe cómo utilizar el ejemplo de script en línea.

**Para usar el ejemplo de script en línea**

1.  Copie la lista MOF de esta sección en un archivo de texto y guárdela con una extensión. mof.
2.  En una ventana del símbolo del sistema, compile el archivo MOF con el siguiente comando.

    Nombre de archivo de **MOFCOMP** ** * *. mof**

El siguiente ejemplo de código MOF crea el filtro, el consumidor y el enlace entre ellos y también contiene el script insertado.

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

 

 
