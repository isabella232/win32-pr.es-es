---
description: Un consumidor lógico es una instancia de una clase de consumidor de eventos permanente.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Crear un consumidor lógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716867"
---
# <a name="creating-a-logical-consumer"></a><span data-ttu-id="83a5a-103">Crear un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="83a5a-103">Creating a Logical Consumer</span></span>

<span data-ttu-id="83a5a-104">Un consumidor lógico es una instancia de una clase de consumidor de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="83a5a-104">A logical consumer is an instance of a permanent event consumer class.</span></span> <span data-ttu-id="83a5a-105">El propósito principal de un consumidor lógico es proporcionar al consumidor físico los parámetros de las actividades que realiza el consumidor físico.</span><span class="sxs-lookup"><span data-stu-id="83a5a-105">The main purpose of a logical consumer is to provide the physical consumer with the parameters for the activities the physical consumer performs.</span></span> <span data-ttu-id="83a5a-106">Para obtener más información, vea [crear una nueva clase de consumidor de eventos permanente](creating-a-new-permanent-event-consumer-class.md).</span><span class="sxs-lookup"><span data-stu-id="83a5a-106">For more information, see [Creating a New Permanent Event Consumer Class](creating-a-new-permanent-event-consumer-class.md).</span></span> <span data-ttu-id="83a5a-107">El consumidor permanente debe tener el mismo [**CreatorSID**](--eventconsumer.md) en las instancias de consumidor, filtro y enlace.</span><span class="sxs-lookup"><span data-stu-id="83a5a-107">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="83a5a-108">Para obtener más información, consulte [recepción de eventos de forma segura](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="83a5a-108">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span> <span data-ttu-id="83a5a-109">Para obtener un ejemplo del uso de un consumidor lógico, vea [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md), que muestra el uso de la clase de consumidor estándar [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para configurar un consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="83a5a-109">For an example of using a logical consumer, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md), which shows the use of the standard consumer class [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to configure a permanent consumer.</span></span>

<span data-ttu-id="83a5a-110">En el procedimiento siguiente se describe cómo crear un consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="83a5a-110">The following procedure describes how to create a logical consumer.</span></span>

<span data-ttu-id="83a5a-111">**Para crear un consumidor lógico**</span><span class="sxs-lookup"><span data-stu-id="83a5a-111">**To create a logical consumer**</span></span>

1.  <span data-ttu-id="83a5a-112">Cree una instancia de la clase de consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="83a5a-112">Create an instance of your permanent consumer class.</span></span>
2.  <span data-ttu-id="83a5a-113">Rellene las propiedades de la instancia con los parámetros de la acción que desea que realice el consumidor físico.</span><span class="sxs-lookup"><span data-stu-id="83a5a-113">Fill the properties of the instance with the parameters of the action you want the physical consumer to perform.</span></span>

<span data-ttu-id="83a5a-114">En el siguiente ejemplo de código MOF se describe un consumidor lógico que contiene un script.</span><span class="sxs-lookup"><span data-stu-id="83a5a-114">The following MOF code example describes a logical consumer that contains a script.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="83a5a-115">Después de crear el consumidor lógico, debe vincular cada filtro a un filtro de eventos para asignar la acción a un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="83a5a-115">After you create the logical consumer, you must then link each filter to an event filter to assign the action to a particular event.</span></span> <span data-ttu-id="83a5a-116">Para obtener más información, vea [crear un filtro de eventos](creating-an-event-filter.md).</span><span class="sxs-lookup"><span data-stu-id="83a5a-116">For more information, see [Creating an Event Filter](creating-an-event-filter.md).</span></span>

 

 



