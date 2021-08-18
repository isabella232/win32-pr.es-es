---
description: Puede crear un objeto para WMI en Visual Basic Scripting Edition (VBScript) si se conecta a WMI y, a continuación, llama a CreateObject. En la tabla siguiente se enumeran los métodos de Scripting API para WMI que admiten la creación de objetos.
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
ms.openlocfilehash: e86dbc649d5feab471485dbdf536cde911c139aeab3b6eb3323b24199438d1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244575"
---
# <a name="creating-an-object-using-vbscript"></a>Crear un objeto mediante VBScript

Puede crear un objeto para WMI en Visual Basic Scripting Edition (VBScript) si se conecta a WMI y, a continuación, llama [a CreateObject](/previous-versions//xzysf6hc(v=vs.85)). En la tabla siguiente se enumeran los métodos de Scripting API para WMI que admiten la creación de objetos.



| Interfaz                                        | ProgID                             |
|--------------------------------------------------|------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)           | "WbemScripting.SwbemDateTime"      |
| [**SWbemLocator**](swbemlocator.md)             | "WbemScripting.SWbemLocator"       |
| [**SWbemLastError**](swbemlasterror.md)         | "WbemScripting.SWbem.LastError"    |
| [**SWbemObjectPath**](swbemobjectpath.md)       | "WbemScripting.SWbemObjectPath"    |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | "WbemScripting.SWbemNamedValueSet" |
| [**SWbemRefresher**](swbemrefresher.md)         | "WbemScripting.SWbemRefresher"     |
| [**SWbemSink**](swbemsink.md)                   | "WbemScripting.SWbemSink"          |



 

En el procedimiento siguiente se describe cómo crear un objeto WMI mediante VBScript.

**Para crear un objeto WMI mediante VBScript**

1.  Conectar a WMI mediante un moniker o [**un objeto SWbemLocator.**](swbemlocator.md)

    Para obtener más información, vea [Crear un script WMI.](creating-a-wmi-script.md)

2.  Realice una llamada al método [CreateObject de](/previous-versions//xzysf6hc(v=vs.85)) VBScript.

    En el ejemplo de código siguiente se muestra cómo crear un objeto .

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Si usa un moniker en el paso 1, no es necesario volver a llamar a [CreateObject.](/previous-versions//xzysf6hc(v=vs.85))

 

 
