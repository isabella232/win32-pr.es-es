---
description: La clase CommandLineEventConsumer ejecuta un programa ejecutable especificado desde una línea de comandos cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Ejecutar un programa desde la línea de comandos en función de un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706090"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a><span data-ttu-id="24179-104">Ejecutar un programa desde la línea de comandos en función de un evento</span><span class="sxs-lookup"><span data-stu-id="24179-104">Running a Program from the Command Line Based on an Event</span></span>

<span data-ttu-id="24179-105">La clase [**CommandLineEventConsumer**](commandlineeventconsumer.md) ejecuta un programa ejecutable especificado desde una línea de comandos cuando se produce un evento especificado.</span><span class="sxs-lookup"><span data-stu-id="24179-105">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class runs a specified executable program from a command line when a specified event occurs.</span></span> <span data-ttu-id="24179-106">Esta clase es un consumidor de eventos estándar que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="24179-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="24179-107">Cuando use [**CommandLineEventConsumer**](commandlineeventconsumer.md), debe proteger el archivo ejecutable que desea iniciar.</span><span class="sxs-lookup"><span data-stu-id="24179-107">When you use [**CommandLineEventConsumer**](commandlineeventconsumer.md), you should secure the executable that you want to start.</span></span> <span data-ttu-id="24179-108">Si el archivo ejecutable no está en una ubicación segura o no está protegido con una lista de control de acceso (ACL) segura, un usuario sin privilegios de acceso puede reemplazar el ejecutable por otro ejecutable diferente.</span><span class="sxs-lookup"><span data-stu-id="24179-108">If the executable is not in a secure location or not secured with a strong access control list (ACL), a user without access privileges can replace your executable with a different executable.</span></span> <span data-ttu-id="24179-109">Puede usar las clases [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) o [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) para cambiar la seguridad de un archivo o recurso compartido mediante programación.</span><span class="sxs-lookup"><span data-stu-id="24179-109">You can use the [**Win32\_LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) or [**Win32\_LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) classes to change programmatically the security of a file or share.</span></span> <span data-ttu-id="24179-110">Para obtener más información, vea [crear un descriptor de seguridad para un nuevo objeto en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="24179-110">For more information, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="24179-111">El procedimiento básico para usar los consumidores estándar siempre es el mismo y se encuentra en [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="24179-111">The basic procedure to use standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="24179-112">El siguiente procedimiento se agrega al procedimiento básico, es específico de la clase [**CommandLineEventConsumer**](commandlineeventconsumer.md) y describe cómo crear un consumidor de eventos que ejecute un programa.</span><span class="sxs-lookup"><span data-stu-id="24179-112">The following procedure adds to the basic procedure, is specific to the [**CommandLineEventConsumer**](commandlineeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

> [!Caution]
>
> <span data-ttu-id="24179-113">La clase [**CommandLineEventConsumer**](commandlineeventconsumer.md) tiene restricciones de seguridad especiales.</span><span class="sxs-lookup"><span data-stu-id="24179-113">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="24179-114">Este consumidor estándar debe configurarlo un miembro local del grupo administradores en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="24179-114">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="24179-115">Si utiliza una cuenta de dominio para crear la suscripción, la cuenta LocalSystem debe tener los permisos necesarios en el dominio para comprobar que el creador es miembro del grupo de administradores locales.</span><span class="sxs-lookup"><span data-stu-id="24179-115">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>
>
> <span data-ttu-id="24179-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) no se puede usar para iniciar un proceso que se ejecuta de forma interactiva.</span><span class="sxs-lookup"><span data-stu-id="24179-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) cannot be used to start a process that runs interactively.</span></span>

 

<span data-ttu-id="24179-117">En el procedimiento siguiente se describe cómo crear un consumidor de eventos que ejecute un proceso desde una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="24179-117">The following procedure describes how to create an event consumer that runs a process from a command line.</span></span>

<span data-ttu-id="24179-118">**Para crear un consumidor de eventos que ejecute un proceso desde una línea de comandos**</span><span class="sxs-lookup"><span data-stu-id="24179-118">**To create an event consumer that runs a process from a command line**</span></span>

1.  <span data-ttu-id="24179-119">En el archivo Managed Object Format (MOF), cree una instancia de [**CommandLineEventConsumer**](commandlineeventconsumer.md) para recibir los eventos que solicita en la consulta.</span><span class="sxs-lookup"><span data-stu-id="24179-119">In the Managed Object Format (MOF) file, create an instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="24179-120">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="24179-120">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="24179-121">Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md) y asígnele un nombre.</span><span class="sxs-lookup"><span data-stu-id="24179-121">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and give it a name.</span></span>
3.  <span data-ttu-id="24179-122">Cree una consulta para especificar el tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="24179-122">Create a query to specify the type of event.</span></span> <span data-ttu-id="24179-123">Para obtener más información, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="24179-123">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>
4.  <span data-ttu-id="24179-124">Cree una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar el filtro a la instancia de [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="24179-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>
5.  <span data-ttu-id="24179-125">Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="24179-125">Compile your MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="24179-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="24179-126">Example</span></span>

<span data-ttu-id="24179-127">En el ejemplo de código siguiente se crea una nueva clase denominada "MyCmdLineConsumer" para generar eventos cuando se crea una instancia de la nueva clase al final de un MOF.</span><span class="sxs-lookup"><span data-stu-id="24179-127">The following code example creates a new class called "MyCmdLineConsumer" to generate events when an instance of the new class is created at the end of a MOF.</span></span> <span data-ttu-id="24179-128">El ejemplo está en código MOF, pero puede crear las instancias mediante programación con la [API de scripting para WMI](scripting-api-for-wmi.md) o la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="24179-128">The example is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="24179-129">En el procedimiento siguiente se describe cómo crear una nueva clase denominada MyCmdLineConsumer.</span><span class="sxs-lookup"><span data-stu-id="24179-129">The following procedure describes how to create a new class called MyCmdLineConsumer.</span></span>

<span data-ttu-id="24179-130">**Para crear una nueva clase denominada MyCmdLineConsumer**</span><span class="sxs-lookup"><span data-stu-id="24179-130">**To create a new class called MyCmdLineConsumer**</span></span>

1.  <span data-ttu-id="24179-131">Cree el archivo c: \\ cmdline \_test.bat con un comando que ejecute un programa visible, como "calc.exe".</span><span class="sxs-lookup"><span data-stu-id="24179-131">Create the c:\\cmdline\_test.bat file with a command that executes a visible program, such as "calc.exe" .</span></span>
2.  <span data-ttu-id="24179-132">Copie el MOF en un archivo de texto y guárdelo con la extensión. mof.</span><span class="sxs-lookup"><span data-stu-id="24179-132">Copy the MOF to a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="24179-133">En un ventana Comandos, compile el archivo MOF con el siguiente comando: **MOFCOMP FILENAME. mof**.</span><span class="sxs-lookup"><span data-stu-id="24179-133">In a Command window, compile the MOF file by using the following command: **Mofcomp filename.mof**.</span></span>

> [!Note]  
> <span data-ttu-id="24179-134">Se debe ejecutar el programa especificado en el \_test.bat cmdline.</span><span class="sxs-lookup"><span data-stu-id="24179-134">The program specified in cmdline\_test.bat should execute.</span></span>

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a><span data-ttu-id="24179-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24179-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24179-136">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="24179-136">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
