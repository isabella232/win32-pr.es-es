---
description: Puede crear un objeto para WMI en Visual Basic Scripting Edition (VBScript) si se conecta a WMI y, a continuación, llama a CreateObject. En la tabla siguiente se enumeran los métodos de la API de scripting para WMI que admiten la creación de objetos.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Crear un objeto mediante VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497770"
---
# <a name="creating-an-object-using-vbscript"></a>Crear un objeto mediante VBScript

Puede crear un objeto para WMI en Visual Basic Scripting Edition (VBScript) si se conecta a WMI y, a continuación, llama a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)). En la tabla siguiente se enumeran los métodos de la API de scripting para WMI que admiten la creación de objetos.



| Interfaz                                        | ProgID                             |
|--------------------------------------------------|------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)           | "WbemScripting.SwbemDateTime"      |
| [**SWbemLocator**](swbemlocator.md)             | "WbemScripting.SWbemLocator"       |
| [**SWbemLastError**](swbemlasterror.md)         | "WbemScripting. SWbem. LastError"    |
| [**SWbemObjectPath**](swbemobjectpath.md)       | "WbemScripting.SWbemObjectPath"    |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | "WbemScripting.SWbemNamedValueSet" |
| [**SWbemRefresher**](swbemrefresher.md)         | "WbemScripting.SWbemRefresher"     |
| [**SWbemSink**](swbemsink.md)                   | "WbemScripting.SWbemSink"          |



 

En el procedimiento siguiente se describe cómo crear un objeto WMI con VBScript.

**Para crear un objeto WMI mediante VBScript**

1.  Conéctese a WMI con un moniker o un objeto [**SWbemLocator**](swbemlocator.md) .

    Para obtener más información, vea [crear un script WMI](creating-a-wmi-script.md).

2.  Realice una llamada al método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.

    En el ejemplo de código siguiente se muestra cómo crear un objeto.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Si utiliza un moniker en el paso 1, no es necesario volver a llamar a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

 

 
