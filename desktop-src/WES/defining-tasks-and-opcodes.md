---
title: Definir tareas y códigos de tarea
description: Los proveedores usan tareas y códigos de operación para agrupar lógicamente los eventos. La agrupación de eventos ayuda a los consumidores a consultar solo los eventos que contienen combinaciones de tareas y OpCode específicas.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257166a34c167d076fec39ac6997d12dc785450
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104533075"
---
# <a name="defining-tasks-and-opcodes"></a>Definir tareas y códigos de tarea

Los proveedores usan tareas y códigos de operación para agrupar lógicamente los eventos. La agrupación de eventos ayuda a los consumidores a consultar solo los eventos que contienen combinaciones de tareas y OpCode específicas. Normalmente, se usan tareas para identificar un componente importante del proveedor, como el componente de red o de base de datos. Después, puede usar códigos de operación para identificar las operaciones que realiza el componente, como las operaciones de envío y recepción para un componente de red. Si solo tenía un componente, puede usar la tarea para reflejar una operación principal en el componente, como conectar o desconectar, y usar el código de operación para reflejar una actividad dentro de la operación, como la lectura del registro. También puede utilizar OpCode sin especificar una tarea. El uso de la tarea y los códigos de desactivación para agrupar los eventos del consumidor es totalmente suya.

Para definir una tarea, use el elemento **Task** . Para definir un código de operación, utilice el elemento **OpCode** . Puede especificar hasta 228 códigos de desactivación. El **valor** de la tarea debe ser mayor que 0. Los códigos de acceso deben estar en el intervalo comprendido entre 11 y 239. El archivo Winmeta.xml define las operaciones comunes que puede usar en lugar de definir las suyas propias.

En el ejemplo siguiente se muestra cómo definir varias tareas y códigos de operaciones.

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
