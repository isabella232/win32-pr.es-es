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
# <a name="creating-a-logical-consumer"></a>Crear un consumidor lógico

Un consumidor lógico es una instancia de una clase de consumidor de eventos permanente. El propósito principal de un consumidor lógico es proporcionar al consumidor físico los parámetros de las actividades que realiza el consumidor físico. Para obtener más información, vea [crear una nueva clase de consumidor de eventos permanente](creating-a-new-permanent-event-consumer-class.md). El consumidor permanente debe tener el mismo [**CreatorSID**](--eventconsumer.md) en las instancias de consumidor, filtro y enlace. Para obtener más información, consulte [recepción de eventos de forma segura](receiving-events-securely.md). Para obtener un ejemplo del uso de un consumidor lógico, vea [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md), que muestra el uso de la clase de consumidor estándar [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para configurar un consumidor permanente.

En el procedimiento siguiente se describe cómo crear un consumidor lógico.

**Para crear un consumidor lógico**

1.  Cree una instancia de la clase de consumidor permanente.
2.  Rellene las propiedades de la instancia con los parámetros de la acción que desea que realice el consumidor físico.

En el siguiente ejemplo de código MOF se describe un consumidor lógico que contiene un script.

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

Después de crear el consumidor lógico, debe vincular cada filtro a un filtro de eventos para asignar la acción a un evento determinado. Para obtener más información, vea [crear un filtro de eventos](creating-an-event-filter.md).

 

 



