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
# <a name="running-a-script-based-on-an-event"></a><span data-ttu-id="2127c-103">Ejecutar un script basado en un evento</span><span class="sxs-lookup"><span data-stu-id="2127c-103">Running a Script Based on an Event</span></span>

<span data-ttu-id="2127c-104">El consumidor estándar implementado por la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) permite a un equipo ejecutar un script y tomar medidas cuando se producen eventos importantes para garantizar que un equipo pueda detectar y resolver problemas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2127c-104">The standard consumer that is implemented by the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class allows a computer to run a script and take action when important events occur to ensure that a computer can detect and resolve problems automatically.</span></span>

<span data-ttu-id="2127c-105">Este consumidor se carga de forma predeterminada en el espacio de nombres de la **\\ suscripción raíz** .</span><span class="sxs-lookup"><span data-stu-id="2127c-105">This consumer is loaded by default in the **root\\subscription** namespace.</span></span>

<span data-ttu-id="2127c-106">Puede configurar el rendimiento de todas las instancias de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) en un sistema estableciendo los valores de la propiedad **timeout** o **MaximumScripts** en una única instancia de [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span><span class="sxs-lookup"><span data-stu-id="2127c-106">You can configure the performance of all instances of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) on a system by setting the values of the **Timeout** or **MaximumScripts** property in a single instance of [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span></span>

<span data-ttu-id="2127c-107">El procedimiento básico para usar consumidores estándar siempre es el mismo y se encuentra en [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="2127c-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="2127c-108">El siguiente procedimiento que agrega al procedimiento básico, es específico de la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) y describe cómo crear un consumidor de eventos que ejecute un script.</span><span class="sxs-lookup"><span data-stu-id="2127c-108">The following procedure that adds to the basic procedure, is specific to the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class, and describes how to create an event consumer that runs a script.</span></span>

> [!Caution]  
> <span data-ttu-id="2127c-109">La clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) tiene restricciones de seguridad especiales.</span><span class="sxs-lookup"><span data-stu-id="2127c-109">The [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="2127c-110">Este consumidor estándar debe configurarlo un miembro local del grupo administradores en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="2127c-110">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="2127c-111">Si utiliza una cuenta de dominio para crear la suscripción, la cuenta LocalSystem debe tener los permisos necesarios en el dominio para comprobar que el creador es miembro del grupo de administradores locales.</span><span class="sxs-lookup"><span data-stu-id="2127c-111">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>

 

<span data-ttu-id="2127c-112">En el procedimiento siguiente se describe cómo crear un consumidor de eventos que ejecute un script.</span><span class="sxs-lookup"><span data-stu-id="2127c-112">The following procedure describes how to create an event consumer that executes a script.</span></span>

<span data-ttu-id="2127c-113">**Para crear un consumidor de eventos que ejecute un script**</span><span class="sxs-lookup"><span data-stu-id="2127c-113">**To create an event consumer that executes a script**</span></span>

1.  <span data-ttu-id="2127c-114">Escribir el script para que se ejecute cuando se produzca un evento.</span><span class="sxs-lookup"><span data-stu-id="2127c-114">Write the script to run when an event takes place.</span></span>

    <span data-ttu-id="2127c-115">Puede escribir el script en cualquier lenguaje, pero asegúrese de que se ha instalado en el equipo un motor de scripting para el idioma que elija.</span><span class="sxs-lookup"><span data-stu-id="2127c-115">You can write the script in any language, but ensure that a scripting engine for the language that you choose is installed on your machine.</span></span> <span data-ttu-id="2127c-116">El script no tiene que utilizar objetos de scripting de WMI.</span><span class="sxs-lookup"><span data-stu-id="2127c-116">The script does not have to use WMI scripting objects.</span></span>

    <span data-ttu-id="2127c-117">Solo un administrador puede configurar un consumidor de scripts y el script se ejecuta con las credenciales LocalSystem, lo que proporciona amplias capacidades al consumidor excepto el acceso a la red.</span><span class="sxs-lookup"><span data-stu-id="2127c-117">Only an administrator can set up a script consumer, and the script runs under LocalSystem credentials, which gives broad capabilities to the consumer except for network access.</span></span> <span data-ttu-id="2127c-118">Sin embargo, el script no tiene acceso a datos de inicio de sesión de usuario específicos, por ejemplo, variables de entorno y recursos compartidos de red.</span><span class="sxs-lookup"><span data-stu-id="2127c-118">However, the script does not have access to specific user logon data, for example, environment variables and network shares.</span></span>

2.  <span data-ttu-id="2127c-119">En el archivo Managed Object Format (MOF), cree una instancia de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para recibir los eventos que solicita en la consulta.</span><span class="sxs-lookup"><span data-stu-id="2127c-119">In the Managed Object Format (MOF) file, create an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to receive the events you request in the query.</span></span>

    <span data-ttu-id="2127c-120">Puede colocar el texto del script en **ScriptText**, o puede especificar la ruta de acceso y el nombre de archivo del script en **ScriptFileName**.</span><span class="sxs-lookup"><span data-stu-id="2127c-120">You can put the text of the script in **ScriptText**, or you can specify the path and filename of the script in **ScriptFileName**.</span></span> <span data-ttu-id="2127c-121">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="2127c-121">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

3.  <span data-ttu-id="2127c-122">Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md), asígnele un nombre y, a continuación, cree una consulta para especificar el tipo de evento, que desencadena la ejecución del script.</span><span class="sxs-lookup"><span data-stu-id="2127c-122">Create an instance of [**\_\_EventFilter**](--eventfilter.md), name it, and then create a query to specify the type of event, which triggers executing the script.</span></span>

    <span data-ttu-id="2127c-123">Para obtener más información, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="2127c-123">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="2127c-124">Cree una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar el filtro a la instancia de [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="2127c-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span></span>
5.  <span data-ttu-id="2127c-125">Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="2127c-125">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

<span data-ttu-id="2127c-126">Los ejemplos de la siguiente sección muestran dos maneras de implementar un script orientado a eventos.</span><span class="sxs-lookup"><span data-stu-id="2127c-126">The examples in the following section show two ways to implement an event-driven script.</span></span> <span data-ttu-id="2127c-127">En el primer ejemplo se usa un script que se define en un archivo externo y en el segundo ejemplo se usa un script integrado en el código MOF.</span><span class="sxs-lookup"><span data-stu-id="2127c-127">The first example uses a script that is defined in an external file, and the second example uses a script that is built into the MOF code.</span></span> <span data-ttu-id="2127c-128">Los ejemplos se encuentran en código MOF, pero puede crear las instancias mediante programación con la API de [scripting para WMI](scripting-api-for-wmi.md) o la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2127c-128">The examples are in MOF code, but you can create the instances programmatically by using either the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

## <a name="example-using-an-external-script"></a><span data-ttu-id="2127c-129">Ejemplo de uso de un script externo</span><span class="sxs-lookup"><span data-stu-id="2127c-129">Example Using an External Script</span></span>

<span data-ttu-id="2127c-130">En el procedimiento siguiente se describe cómo usar el ejemplo de script externo.</span><span class="sxs-lookup"><span data-stu-id="2127c-130">The following procedure describes how to use the external script example.</span></span>

<span data-ttu-id="2127c-131">**Para usar el ejemplo de script externo**</span><span class="sxs-lookup"><span data-stu-id="2127c-131">**To use the external script example**</span></span>

1.  <span data-ttu-id="2127c-132">Cree un archivo denominado c: \\Asec.vbs y, a continuación, copie en él el script de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2127c-132">Create a file named c:\\Asec.vbs, and then copy the script in this example into it.</span></span>
2.  <span data-ttu-id="2127c-133">Copie la lista MOF en un archivo de texto y guárdela con una extensión. mof.</span><span class="sxs-lookup"><span data-stu-id="2127c-133">Copy the MOF list into a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="2127c-134">En una ventana del símbolo del sistema, compile el archivo MOF con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="2127c-134">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="2127c-135">Nombre de archivo de **MOFCOMP** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="2127c-135">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

4.  <span data-ttu-id="2127c-136">Ejecute la calculadora, que crea un proceso de calc.exe.</span><span class="sxs-lookup"><span data-stu-id="2127c-136">Run the Calculator, which creates a calc.exe process.</span></span> <span data-ttu-id="2127c-137">Espere más de cinco segundos, cierre la ventana calculadora y busque en el directorio C: \\ un archivo denominado ASEC. log.</span><span class="sxs-lookup"><span data-stu-id="2127c-137">Wait for more than five seconds, close the Calculator window, and then look in the C:\\ directory for a file named ASEC.log.</span></span>

    <span data-ttu-id="2127c-138">El texto siguiente es similar al texto que se incluirá en el archivo ASEC. log.</span><span class="sxs-lookup"><span data-stu-id="2127c-138">The following text is similar to the text that will be contained in the ASEC.log file.</span></span>

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

<span data-ttu-id="2127c-139">En el siguiente ejemplo de código de VBScript se muestra el script al que se llama cuando el consumidor permanente recibe un evento.</span><span class="sxs-lookup"><span data-stu-id="2127c-139">The following VBScript code example shows the script that is called when an event is received by the permanent consumer.</span></span> <span data-ttu-id="2127c-140">El objeto **TargetEvent** es una instancia de [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) , por lo que tiene una propiedad denominada **TargetInstance**, que es una instancia de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que se usa para desencadenar el evento.</span><span class="sxs-lookup"><span data-stu-id="2127c-140">The **TargetEvent** object is an [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) instance so it has a property named **TargetInstance**, which is a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instance used to fire the event.</span></span> <span data-ttu-id="2127c-141">La clase de **\_ proceso de Win32** tiene las propiedades **UserModeTime** y **KernelModeTime** que se colocan en el archivo de registro creado por el script.</span><span class="sxs-lookup"><span data-stu-id="2127c-141">The **Win32\_Process** class has the **UserModeTime** and **KernelModeTime** properties that are put into the log file created by the script.</span></span>


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



<span data-ttu-id="2127c-142">El siguiente ejemplo de código MOF llama al script cuando se recibe un evento.</span><span class="sxs-lookup"><span data-stu-id="2127c-142">The following MOF code example calls the script when an event is received.</span></span> <span data-ttu-id="2127c-143">Crea el filtro, el consumidor y el enlace entre ellos en el espacio de nombres de la **\\ suscripción raíz** .</span><span class="sxs-lookup"><span data-stu-id="2127c-143">It creates the filter, consumer, and the binding between them in the **root\\subscription** namespace.</span></span>

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

## <a name="example-using-inline-script"></a><span data-ttu-id="2127c-144">Ejemplo con el script en línea</span><span class="sxs-lookup"><span data-stu-id="2127c-144">Example Using Inline Script</span></span>

<span data-ttu-id="2127c-145">En el procedimiento siguiente se describe cómo utilizar el ejemplo de script en línea.</span><span class="sxs-lookup"><span data-stu-id="2127c-145">The following procedure describes how to use the inline script example.</span></span>

<span data-ttu-id="2127c-146">**Para usar el ejemplo de script en línea**</span><span class="sxs-lookup"><span data-stu-id="2127c-146">**To use the inline script example**</span></span>

1.  <span data-ttu-id="2127c-147">Copie la lista MOF de esta sección en un archivo de texto y guárdela con una extensión. mof.</span><span class="sxs-lookup"><span data-stu-id="2127c-147">Copy the MOF list in this section into a text file, and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="2127c-148">En una ventana del símbolo del sistema, compile el archivo MOF con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="2127c-148">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="2127c-149">Nombre de archivo de **MOFCOMP** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="2127c-149">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

<span data-ttu-id="2127c-150">El siguiente ejemplo de código MOF crea el filtro, el consumidor y el enlace entre ellos y también contiene el script insertado.</span><span class="sxs-lookup"><span data-stu-id="2127c-150">The following MOF code example creates the filter, consumer, and the binding between them and also contains the script inline.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2127c-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2127c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2127c-152">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="2127c-152">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
