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
# <a name="defining-tasks-and-opcodes"></a><span data-ttu-id="e2181-104">Definir tareas y códigos de tarea</span><span class="sxs-lookup"><span data-stu-id="e2181-104">Defining Tasks and Opcodes</span></span>

<span data-ttu-id="e2181-105">Los proveedores usan tareas y códigos de operación para agrupar lógicamente los eventos.</span><span class="sxs-lookup"><span data-stu-id="e2181-105">Providers use tasks and opcodes to logically group events.</span></span> <span data-ttu-id="e2181-106">La agrupación de eventos ayuda a los consumidores a consultar solo los eventos que contienen combinaciones de tareas y OpCode específicas.</span><span class="sxs-lookup"><span data-stu-id="e2181-106">Grouping events helps consumers query for only those events that contain specific task and opcode combinations.</span></span> <span data-ttu-id="e2181-107">Normalmente, se usan tareas para identificar un componente importante del proveedor, como el componente de red o de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e2181-107">Typically, you use tasks to identify a major component of the provider such as the networking or database component.</span></span> <span data-ttu-id="e2181-108">Después, puede usar códigos de operación para identificar las operaciones que realiza el componente, como las operaciones de envío y recepción para un componente de red.</span><span class="sxs-lookup"><span data-stu-id="e2181-108">You could then use opcodes to identify the operations that the component performs, such as the send and receive operations for a networking component.</span></span> <span data-ttu-id="e2181-109">Si solo tenía un componente, puede usar la tarea para reflejar una operación principal en el componente, como conectar o desconectar, y usar el código de operación para reflejar una actividad dentro de la operación, como la lectura del registro.</span><span class="sxs-lookup"><span data-stu-id="e2181-109">If you had only one component, you could use task to reflect a major operation in the component, such as connect or disconnect, and use opcode to reflect an activity within the operation such as reading the registry.</span></span> <span data-ttu-id="e2181-110">También puede utilizar OpCode sin especificar una tarea.</span><span class="sxs-lookup"><span data-stu-id="e2181-110">You could also use opcode without specifying a task.</span></span> <span data-ttu-id="e2181-111">El uso de la tarea y los códigos de desactivación para agrupar los eventos del consumidor es totalmente suya.</span><span class="sxs-lookup"><span data-stu-id="e2181-111">How you use task and opcodes to group events for the consumer is completely up to you.</span></span>

<span data-ttu-id="e2181-112">Para definir una tarea, use el elemento **Task** .</span><span class="sxs-lookup"><span data-stu-id="e2181-112">To define a task, use the **task** element.</span></span> <span data-ttu-id="e2181-113">Para definir un código de operación, utilice el elemento **OpCode** .</span><span class="sxs-lookup"><span data-stu-id="e2181-113">To define an opcode, use the **opcode** element.</span></span> <span data-ttu-id="e2181-114">Puede especificar hasta 228 códigos de desactivación.</span><span class="sxs-lookup"><span data-stu-id="e2181-114">You can specify up to 228 opcodes.</span></span> <span data-ttu-id="e2181-115">El **valor** de la tarea debe ser mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="e2181-115">The task **value** must be greater than 0.</span></span> <span data-ttu-id="e2181-116">Los códigos de acceso deben estar en el intervalo comprendido entre 11 y 239.</span><span class="sxs-lookup"><span data-stu-id="e2181-116">The opcodes must be in the range from 11 through 239.</span></span> <span data-ttu-id="e2181-117">El archivo Winmeta.xml define las operaciones comunes que puede usar en lugar de definir las suyas propias.</span><span class="sxs-lookup"><span data-stu-id="e2181-117">The Winmeta.xml file defines common operations that you can use instead of defining your own.</span></span>

<span data-ttu-id="e2181-118">En el ejemplo siguiente se muestra cómo definir varias tareas y códigos de operaciones.</span><span class="sxs-lookup"><span data-stu-id="e2181-118">The following example shows how to define several tasks and opcodes.</span></span>

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
