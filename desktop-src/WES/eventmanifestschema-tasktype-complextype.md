---
title: Tipo complejo de TaskType
description: Define un componente o subcomponente de una aplicación. | Tipo complejo de TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- Registro de eventos de tipo complejo TaskType
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698161"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="08384-105">Tipo complejo de TaskType</span><span class="sxs-lookup"><span data-stu-id="08384-105">TaskType Complex Type</span></span>

<span data-ttu-id="08384-106">Define un componente o subcomponente de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="08384-106">Defines a component or subcomponent of an application.</span></span>

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="08384-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08384-107">Child elements</span></span>



| <span data-ttu-id="08384-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="08384-108">Element</span></span>                                                         | <span data-ttu-id="08384-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="08384-109">Type</span></span>                                                                     | <span data-ttu-id="08384-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="08384-110">Description</span></span>                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08384-111">**códigos**</span><span class="sxs-lookup"><span data-stu-id="08384-111">**opcodes**</span></span>](eventmanifestschema-opcodes-tasktype-element.md) | [<span data-ttu-id="08384-112">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="08384-112">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md) | <span data-ttu-id="08384-113">Define una lista de códigos de tiempo específicos de la tarea.</span><span class="sxs-lookup"><span data-stu-id="08384-113">Defines a list of task-specific opcodes.</span></span> <span data-ttu-id="08384-114">No se pueden usar los valores de OpCode definidos en Winmeta.xml para códigos de operación específicos de la tarea.</span><span class="sxs-lookup"><span data-stu-id="08384-114">You cannot use the opcode values defined in Winmeta.xml for task-specific opcodes.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="08384-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="08384-115">Attributes</span></span>



| <span data-ttu-id="08384-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="08384-116">Name</span></span>      | <span data-ttu-id="08384-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="08384-117">Type</span></span>                                                              | <span data-ttu-id="08384-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="08384-118">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08384-119">eventGUID</span><span class="sxs-lookup"><span data-stu-id="08384-119">eventGUID</span></span> | [<span data-ttu-id="08384-120">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="08384-120">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="08384-121">Identificador único global, en formato de registro, que identifica la tarea.</span><span class="sxs-lookup"><span data-stu-id="08384-121">A globally unique identifier, in Registry format, that identifies the task.</span></span> <span data-ttu-id="08384-122">Este atributo es necesario si se usa el argumento del compilador de mensajes MOF para generar una clase MOF para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="08384-122">This attribute is required if you use the -mof message compiler argument to generate a MOF class for downlevel support.</span></span><br/>                                                                                                   |
| <span data-ttu-id="08384-123">message</span><span class="sxs-lookup"><span data-stu-id="08384-123">message</span></span>   | [<span data-ttu-id="08384-124">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="08384-124">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="08384-125">Nombre para mostrar localizado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="08384-125">The localized display name for the task.</span></span> <span data-ttu-id="08384-126">La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="08384-126">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                   |
| <span data-ttu-id="08384-127">name</span><span class="sxs-lookup"><span data-stu-id="08384-127">name</span></span>      | <span data-ttu-id="08384-128">**QName**</span><span class="sxs-lookup"><span data-stu-id="08384-128">**QName**</span></span>                                                         | <span data-ttu-id="08384-129">Nombre de la tarea.</span><span class="sxs-lookup"><span data-stu-id="08384-129">The name of the task.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="08384-130">símbolo</span><span class="sxs-lookup"><span data-stu-id="08384-130">symbol</span></span>    | [<span data-ttu-id="08384-131">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="08384-131">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="08384-132">Símbolo que se va a usar para hacer referencia a la tarea en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="08384-132">The symbol to use to reference the task in your application.</span></span> <span data-ttu-id="08384-133">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la tarea en el archivo de encabezado generado por el compilador.</span><span class="sxs-lookup"><span data-stu-id="08384-133">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the task in the header file that the compiler generates.</span></span> <span data-ttu-id="08384-134">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="08384-134">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="08384-135">value</span><span class="sxs-lookup"><span data-stu-id="08384-135">value</span></span>     | [<span data-ttu-id="08384-136">**UInt16Type**</span><span class="sxs-lookup"><span data-stu-id="08384-136">**UInt16Type**</span></span>](eventmanifestschema-hexint16type-simpletype.md) | <span data-ttu-id="08384-137">Valor numérico que identifica de forma única esta tarea en la lista de tareas que define el proveedor.</span><span class="sxs-lookup"><span data-stu-id="08384-137">A numeric value that uniquely identifies this task within the list of tasks that the provider defines.</span></span> <span data-ttu-id="08384-138">El valor debe estar en el intervalo comprendido entre 1 y 239.</span><span class="sxs-lookup"><span data-stu-id="08384-138">The value must be in the range from 1 through 239.</span></span><br/>                                                                                                                                             |



## <a name="examples"></a><span data-ttu-id="08384-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="08384-139">Examples</span></span>

<span data-ttu-id="08384-140">En el ejemplo siguiente se muestra cómo especificar una tarea.</span><span class="sxs-lookup"><span data-stu-id="08384-140">The following example shows how to specify a task.</span></span>


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a><span data-ttu-id="08384-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08384-141">Requirements</span></span>



| <span data-ttu-id="08384-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="08384-142">Requirement</span></span> | <span data-ttu-id="08384-143">Value</span><span class="sxs-lookup"><span data-stu-id="08384-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="08384-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08384-144">Minimum supported client</span></span><br/> | <span data-ttu-id="08384-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="08384-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="08384-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08384-146">Minimum supported server</span></span><br/> | <span data-ttu-id="08384-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="08384-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





