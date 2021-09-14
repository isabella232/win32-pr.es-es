---
title: Definir tareas y códigos de operación
description: Los proveedores usan tareas y códigos de operación para agrupar eventos de forma lógica. La agrupación de eventos ayuda a los consumidores a consultar solo aquellos eventos que contienen combinaciones específicas de tareas y códigos de operación.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257166a34c167d076fec39ac6997d12dc785450
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885500"
---
# <a name="defining-tasks-and-opcodes"></a>Definir tareas y códigos de operación

Los proveedores usan tareas y códigos de operación para agrupar eventos de forma lógica. La agrupación de eventos ayuda a los consumidores a consultar solo aquellos eventos que contienen combinaciones específicas de tareas y códigos de operación. Normalmente, se usan tareas para identificar un componente principal del proveedor, como el componente de red o base de datos. A continuación, podría usar códigos de operación para identificar las operaciones que realiza el componente, como las operaciones de envío y recepción de un componente de red. Si solo tuviera un componente, podría usar la tarea para reflejar una operación principal en el componente, como conectarse o desconectarse, y usar el código de operación para reflejar una actividad dentro de la operación, como leer el Registro. También puede usar el código de operación sin especificar una tarea. El uso de tareas y códigos de operación para agrupar eventos para el consumidor es totalmente su función.

Para definir una tarea, use el **elemento task.** Para definir un código de operación, use el **elemento opcode.** Puede especificar hasta 228 códigos de operación. El valor **de la** tarea debe ser mayor que 0. Los códigos de operación deben estar en el intervalo de 11 a 239. El Winmeta.xml archivo define operaciones comunes que puede usar en lugar de definir las suyas propias.

En el ejemplo siguiente se muestra cómo definir varias tareas y códigos de operación.

```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <tasks>
                    <task name="Disconnect" 
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>
 
                    <task name="Connect" 
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)">
                    </task>

                    <task name="Validate" 
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)">
                    </task>
                </tasks>

                <opcodes>
                    <opcode name="Initialize" 
                            symbol="OPCODE_INITIALIZE" 
                            value="12"
                            message="$(string.Opcode.Initialize)"/>

                    <opcode name="Cleanup" 
                            symbol="OPCODE_CLEANUP" 
                            value="13"
                            message="$(string.Opcode.Cleanup)"/>
                 </opcodes>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
