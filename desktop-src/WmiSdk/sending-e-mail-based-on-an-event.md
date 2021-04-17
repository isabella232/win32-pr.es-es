---
description: Mediante el uso de la clase SMTPEventConsumer, puede enviar un correo electrónico a un usuario designado cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Envío de correo electrónico basado en un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706460"
---
# <a name="sending-email-based-on-an-event"></a><span data-ttu-id="9ffa6-104">Envío de correo electrónico basado en un evento</span><span class="sxs-lookup"><span data-stu-id="9ffa6-104">Sending Email Based on an Event</span></span>

<span data-ttu-id="9ffa6-105">Mediante el uso de la clase [SMTPEventConsumer](smtpeventconsumer.md) , puede enviar un correo electrónico a un usuario designado cuando se produce un evento especificado.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-105">By using the [SMTPEventConsumer](smtpeventconsumer.md) class, you can send email to a designated user when a specified event occurs.</span></span> <span data-ttu-id="9ffa6-106">Esta clase es un [consumidor de eventos estándar](standard-consumer-classes.md) que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-106">This class is a [standard event consumer](standard-consumer-classes.md) that WMI provides.</span></span>

<span data-ttu-id="9ffa6-107">La clase [SMTPEventConsumer](smtpeventconsumer.md) requiere las siguientes condiciones para enviar un mensaje de correo electrónico en respuesta a un evento:</span><span class="sxs-lookup"><span data-stu-id="9ffa6-107">The [SMTPEventConsumer](smtpeventconsumer.md) class requires the following conditions to send an email message in response to an event:</span></span>

-   <span data-ttu-id="9ffa6-108">La clase [SMTPEventConsumer](smtpeventconsumer.md) se debe compilar en el espacio de nombres correcto.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-108">The [SMTPEventConsumer](smtpeventconsumer.md) class must be compiled into the correct namespace.</span></span> <span data-ttu-id="9ffa6-109">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-109">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>
-   <span data-ttu-id="9ffa6-110">Debe existir un servidor SMTP en la red.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-110">An SMTP server must exist on the network.</span></span>
-   <span data-ttu-id="9ffa6-111">El mensaje de correo electrónico no puede tener datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-111">The email message cannot have an attachment.</span></span>
-   <span data-ttu-id="9ffa6-112">El mensaje de correo electrónico debe estar codificado en US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-112">The email message must be encoded in US-ASCII.</span></span>

<span data-ttu-id="9ffa6-113">El procedimiento básico para usar consumidores estándar siempre es el mismo y se encuentra en [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-113">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="9ffa6-114">El siguiente procedimiento se agrega al procedimiento básico: es específico de la clase [SMTPEventConsumer](smtpeventconsumer.md) ; y describe cómo crear un consumidor de eventos que envíe correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-114">The following procedure adds to the basic procedure; is specific to the [SMTPEventConsumer](smtpeventconsumer.md) class; and describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="9ffa6-115">En el procedimiento siguiente se describe cómo crear un consumidor de eventos que envíe correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-115">The following procedure describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="9ffa6-116">**Para crear un consumidor de eventos que envíe correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="9ffa6-116">**To create an event consumer that sends email**</span></span>

1.  <span data-ttu-id="9ffa6-117">Instale y registre la clase [SMTPEventConsumer](smtpeventconsumer.md) , si es necesario.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-117">Install and register the [SMTPEventConsumer](smtpeventconsumer.md) class, if necessary.</span></span>

    <span data-ttu-id="9ffa6-118">El programa de instalación de WMI compila la clase [SMTPEventConsumer](smtpeventconsumer.md) en el espacio de nombres de la \\ suscripción raíz.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-118">The [SMTPEventConsumer](smtpeventconsumer.md) class is compiled into the root\\subscription namespace by the WMI setup program.</span></span>

2.  <span data-ttu-id="9ffa6-119">Identifique el evento que desea supervisar y cree la consulta de eventos.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-119">Identify the event that you want to monitor and create the event query.</span></span>

    <span data-ttu-id="9ffa6-120">Puede haber un evento intrínseco existente que use para supervisar el evento.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-120">There might be an existing intrinsic event that use to monitor your event.</span></span> <span data-ttu-id="9ffa6-121">La mayoría de los eventos intrínsecos se asocian a los cambios en las instancias de clase en el espacio de nombres "root \\ cimv2".</span><span class="sxs-lookup"><span data-stu-id="9ffa6-121">Most intrinsic events are associated with changes to class instances in the "root\\cimv2" namespace.</span></span> <span data-ttu-id="9ffa6-122">Mediante el análisis de las clases de la referencia de [las clases de WMI](wmi-classes.md) , es probable que encuentre una clase que identifique el evento que desea supervisar.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-122">By analyzing the classes in the [WMI Classes](wmi-classes.md) reference, you can probably find a class that identifies the event you want to monitor.</span></span> <span data-ttu-id="9ffa6-123">Por ejemplo, utilice la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) para supervisar los cambios en una unidad de disco duro.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-123">For example, use the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class to monitor changes to a hard disk drive.</span></span>

    <span data-ttu-id="9ffa6-124">Si no hay ningún evento intrínseco existente que use, puede haber un proveedor de eventos extrínsecos que pueda funcionar.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-124">If there are no existing intrinsic events that use, there might be an extrinsic event provider that can work.</span></span> <span data-ttu-id="9ffa6-125">Por ejemplo, utilice la clase [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del proveedor del registro para supervisar los cambios en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-125">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="9ffa6-126">Si no existe una clase que identifique el evento que desea supervisar, debe crear su propio proveedor de eventos y definir nuevas clases de eventos extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-126">If a class does not exist that identifies the event you want to monitor, you must create your own event provider and define new extrinsic event classes.</span></span> <span data-ttu-id="9ffa6-127">Para obtener más información, consulte [escribir un proveedor de eventos](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-127">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

3.  <span data-ttu-id="9ffa6-128">En el archivo Managed Object Format (MOF), cree una instancia de [SMTPEventConsumer](smtpeventconsumer.md) para recibir eventos.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-128">In the Managed Object Format (MOF) file, create an instance of the [SMTPEventConsumer](smtpeventconsumer.md) to receive events.</span></span>

    <span data-ttu-id="9ffa6-129">Use las propiedades de la instancia de para definir el mensaje de correo electrónico que se enviará cuando se produzca un evento.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-129">Use the properties of the instance to define the email message to send when an event occurs.</span></span> <span data-ttu-id="9ffa6-130">Por ejemplo, la propiedad **ToLine** define la dirección de correo electrónico y la propiedad **Message** define el texto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-130">For example, the **ToLine** property defines the email address, and the **Message** property defines the text of the email message.</span></span> <span data-ttu-id="9ffa6-131">Debe definir la dirección de correo electrónico, el asunto y el texto de un mensaje, pero un mensaje de correo electrónico no puede tener datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-131">You must define the email address, subject, and text of a message, but an email message cannot have an attachment.</span></span> <span data-ttu-id="9ffa6-132">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-132">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

4.  <span data-ttu-id="9ffa6-133">Cree una consulta de evento que especifique los eventos que desea supervisar.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-133">Create an event query that specifies the events you want to monitor.</span></span>

    <span data-ttu-id="9ffa6-134">Para obtener más información, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-134">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

5.  <span data-ttu-id="9ffa6-135">Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md) y almacene la consulta en la propiedad **query** .</span><span class="sxs-lookup"><span data-stu-id="9ffa6-135">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and store your query in the **Query** property.</span></span>

    <span data-ttu-id="9ffa6-136">Para obtener más información, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-136">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

6.  <span data-ttu-id="9ffa6-137">Cree una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar el filtro y el consumidor.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-137">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer.</span></span>
7.  <span data-ttu-id="9ffa6-138">Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-138">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>


## <a name="example"></a><span data-ttu-id="9ffa6-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ffa6-139">Example</span></span>

<span data-ttu-id="9ffa6-140">El ejemplo de esta sección está en código MOF, pero puede crear las instancias mediante programación con la API de [scripting para WMI](scripting-api-for-wmi.md) o la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-140">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="9ffa6-141">En el procedimiento siguiente se describe cómo utilizar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-141">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="9ffa6-142">**Para usar el ejemplo**</span><span class="sxs-lookup"><span data-stu-id="9ffa6-142">**To use the example**</span></span>

1.  <span data-ttu-id="9ffa6-143">Copie el MOF siguiente en un archivo de texto y guárdelo con una extensión. mof.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-143">Copy the following MOF to a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="9ffa6-144">En una ventana del símbolo del sistema, compile el archivo MOF con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="9ffa6-144">In a command prompt window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="9ffa6-145">Nombre de archivo de **MOFCOMP** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="9ffa6-145">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

> [!Note]  
> <span data-ttu-id="9ffa6-146">Cuando el código MOF se compila en el \\ espacio de nombres de la suscripción raíz, el [SMTPEventConsumer](smtpeventconsumer.md) se compila en el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-146">When MOF code is compiled into the root\\subscription namespace, the [SMTPEventConsumer](smtpeventconsumer.md) is compiled into the same namespace.</span></span>

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a><span data-ttu-id="9ffa6-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ffa6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ffa6-148">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="9ffa6-148">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
