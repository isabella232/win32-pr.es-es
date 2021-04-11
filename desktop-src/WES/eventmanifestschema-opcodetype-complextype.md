---
title: Tipo complejo de OpcodeType
description: Define una operación dentro de un componente de la aplicación.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- OpcodeType tipo complejo EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151067"
---
# <a name="opcodetype-complex-type"></a><span data-ttu-id="74862-104">Tipo complejo de OpcodeType</span><span class="sxs-lookup"><span data-stu-id="74862-104">OpcodeType Complex Type</span></span>

<span data-ttu-id="74862-105">Define una operación dentro de un componente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74862-105">Defines an operation within a component of the application.</span></span> <span data-ttu-id="74862-106">Se usa junto con una tarea para identificar la sección de la aplicación que está registrando el evento.</span><span class="sxs-lookup"><span data-stu-id="74862-106">Used in conjunction with a task to identify the section of the application that is logging the event.</span></span>

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
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
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="74862-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="74862-107">Attributes</span></span>



| <span data-ttu-id="74862-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="74862-108">Name</span></span>     | <span data-ttu-id="74862-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="74862-109">Type</span></span>                                                              | <span data-ttu-id="74862-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="74862-110">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74862-111">message</span><span class="sxs-lookup"><span data-stu-id="74862-111">message</span></span>  | [<span data-ttu-id="74862-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="74862-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="74862-113">Nombre para mostrar localizado del código de operación.</span><span class="sxs-lookup"><span data-stu-id="74862-113">The localized display name for the opcode.</span></span> <span data-ttu-id="74862-114">La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="74862-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                     |
| <span data-ttu-id="74862-115">mofValue</span><span class="sxs-lookup"><span data-stu-id="74862-115">mofValue</span></span> | [<span data-ttu-id="74862-116">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="74862-116">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="74862-117">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="74862-117">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="74862-118">name</span><span class="sxs-lookup"><span data-stu-id="74862-118">name</span></span>     | <span data-ttu-id="74862-119">**QName**</span><span class="sxs-lookup"><span data-stu-id="74862-119">**QName**</span></span>                                                         | <span data-ttu-id="74862-120">Nombre del código de operación.</span><span class="sxs-lookup"><span data-stu-id="74862-120">The name of the opcode.</span></span> <span data-ttu-id="74862-121">Este nombre debe ser único dentro del ámbito de este proveedor.</span><span class="sxs-lookup"><span data-stu-id="74862-121">This name must be unique within the scope of this provider.</span></span> <br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="74862-122">símbolo</span><span class="sxs-lookup"><span data-stu-id="74862-122">symbol</span></span>   | [<span data-ttu-id="74862-123">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="74862-123">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="74862-124">Símbolo que se va a usar para hacer referencia al código de operación en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74862-124">The symbol to use to reference the opcode in your application.</span></span> <span data-ttu-id="74862-125">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el código de operación en el archivo de encabezado generado por el compilador.</span><span class="sxs-lookup"><span data-stu-id="74862-125">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the opcode in the header file that the compiler generates.</span></span> <span data-ttu-id="74862-126">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="74862-126">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="74862-127">value</span><span class="sxs-lookup"><span data-stu-id="74862-127">value</span></span>    | [<span data-ttu-id="74862-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="74862-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="74862-129">Valor de código de operación.</span><span class="sxs-lookup"><span data-stu-id="74862-129">The opcode value.</span></span> <span data-ttu-id="74862-130">Puede especificar valores en el rango 10 y 239.</span><span class="sxs-lookup"><span data-stu-id="74862-130">You can specify values in the range 10 and 239.</span></span> <span data-ttu-id="74862-131">Para obtener una lista de valores de código de operación predefinidos, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="74862-131">For a list of predefined opcode values, see Remarks.</span></span><br/>                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="74862-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74862-132">Remarks</span></span>

<span data-ttu-id="74862-133">A continuación se muestran los valores de código de operación predefinidos que puede usar.</span><span class="sxs-lookup"><span data-stu-id="74862-133">The following are the predefined opcode values that you can use.</span></span> <span data-ttu-id="74862-134">Estos valores se definen en el archivo Winmeta.xml que se incluye en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="74862-134">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="74862-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="74862-135">Name</span></span>          | <span data-ttu-id="74862-136">Value</span><span class="sxs-lookup"><span data-stu-id="74862-136">Value</span></span> | <span data-ttu-id="74862-137">Símbolo</span><span class="sxs-lookup"><span data-stu-id="74862-137">Symbol</span></span>                      | <span data-ttu-id="74862-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="74862-138">Description</span></span>                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74862-139">Win: info</span><span class="sxs-lookup"><span data-stu-id="74862-139">win:Info</span></span>      | <span data-ttu-id="74862-140">0</span><span class="sxs-lookup"><span data-stu-id="74862-140">0</span></span>     | <span data-ttu-id="74862-141">información de código de operación de WINEVENT \_ \_</span><span class="sxs-lookup"><span data-stu-id="74862-141">WINEVENT\_OPCODE\_INFO</span></span>      | <span data-ttu-id="74862-142">Evento de información.</span><span class="sxs-lookup"><span data-stu-id="74862-142">An informational event.</span></span>                                                                                |
| <span data-ttu-id="74862-143">Win: Inicio</span><span class="sxs-lookup"><span data-stu-id="74862-143">win:Start</span></span>     | <span data-ttu-id="74862-144">1</span><span class="sxs-lookup"><span data-stu-id="74862-144">1</span></span>     | <span data-ttu-id="74862-145">\_Inicio del código de operación WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="74862-145">WINEVENT\_OPCODE\_START</span></span>     | <span data-ttu-id="74862-146">Un evento que representa el inicio de una actividad.</span><span class="sxs-lookup"><span data-stu-id="74862-146">An event that represents starting an activity.</span></span>                                                         |
| <span data-ttu-id="74862-147">Win: detener</span><span class="sxs-lookup"><span data-stu-id="74862-147">win:Stop</span></span>      | <span data-ttu-id="74862-148">2</span><span class="sxs-lookup"><span data-stu-id="74862-148">2</span></span>     | <span data-ttu-id="74862-149">\_detención del código de operación WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="74862-149">WINEVENT\_OPCODE\_STOP</span></span>      | <span data-ttu-id="74862-150">Un evento que representa la detención de una actividad.</span><span class="sxs-lookup"><span data-stu-id="74862-150">An event that represents stopping an activity.</span></span> <span data-ttu-id="74862-151">El evento corresponde al último evento de inicio no emparejado.</span><span class="sxs-lookup"><span data-stu-id="74862-151">The event corresponds to the last unpaired start event.</span></span> |
| <span data-ttu-id="74862-152">Win: Inicio de DC \_</span><span class="sxs-lookup"><span data-stu-id="74862-152">win:DC\_Start</span></span> | <span data-ttu-id="74862-153">3</span><span class="sxs-lookup"><span data-stu-id="74862-153">3</span></span>     | <span data-ttu-id="74862-154">Inicio de WINEVENT \_ OPCODE de \_ DC \_</span><span class="sxs-lookup"><span data-stu-id="74862-154">WINEVENT\_OPCODE\_DC\_START</span></span> | <span data-ttu-id="74862-155">Evento que representa el inicio de la recolección de datos.</span><span class="sxs-lookup"><span data-stu-id="74862-155">An event that represents data collection starting.</span></span> <span data-ttu-id="74862-156">Estos son los tipos de evento de detención.</span><span class="sxs-lookup"><span data-stu-id="74862-156">These are rundown event types.</span></span>                      |
| <span data-ttu-id="74862-157">Win: detención de DC \_</span><span class="sxs-lookup"><span data-stu-id="74862-157">win:DC\_Stop</span></span>  | <span data-ttu-id="74862-158">4</span><span class="sxs-lookup"><span data-stu-id="74862-158">4</span></span>     | <span data-ttu-id="74862-159">detención de DC del código de \_ operación WINEVENT \_ \_</span><span class="sxs-lookup"><span data-stu-id="74862-159">WINEVENT\_OPCODE\_DC\_STOP</span></span>  | <span data-ttu-id="74862-160">Evento que representa la detención de la recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="74862-160">An event that represents data collection stopping.</span></span> <span data-ttu-id="74862-161">Estos son los tipos de evento de detención.</span><span class="sxs-lookup"><span data-stu-id="74862-161">These are rundown event types.</span></span>                      |
| <span data-ttu-id="74862-162">Win: extensión</span><span class="sxs-lookup"><span data-stu-id="74862-162">win:Extension</span></span> | <span data-ttu-id="74862-163">5</span><span class="sxs-lookup"><span data-stu-id="74862-163">5</span></span>     | <span data-ttu-id="74862-164">WINEVENT ( \_ extensión de código de operación) \_</span><span class="sxs-lookup"><span data-stu-id="74862-164">WINEVENT\_OPCODE\_EXTENSION</span></span> | <span data-ttu-id="74862-165">Evento de extensión.</span><span class="sxs-lookup"><span data-stu-id="74862-165">An extension event.</span></span>                                                                                    |
| <span data-ttu-id="74862-166">Win: responder</span><span class="sxs-lookup"><span data-stu-id="74862-166">win:Reply</span></span>     | <span data-ttu-id="74862-167">6</span><span class="sxs-lookup"><span data-stu-id="74862-167">6</span></span>     | <span data-ttu-id="74862-168">\_respuesta de código de operación WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="74862-168">WINEVENT\_OPCODE\_REPLY</span></span>     | <span data-ttu-id="74862-169">Un evento de respuesta.</span><span class="sxs-lookup"><span data-stu-id="74862-169">A reply event.</span></span>                                                                                         |
| <span data-ttu-id="74862-170">Win: currículum</span><span class="sxs-lookup"><span data-stu-id="74862-170">win:Resume</span></span>    | <span data-ttu-id="74862-171">7</span><span class="sxs-lookup"><span data-stu-id="74862-171">7</span></span>     | <span data-ttu-id="74862-172">\_reanudación del código de operación WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="74862-172">WINEVENT\_OPCODE\_RESUME</span></span>    | <span data-ttu-id="74862-173">Un evento que representa una actividad que se reanuda después de suspenderse.</span><span class="sxs-lookup"><span data-stu-id="74862-173">An event that represents an activity resuming after being suspended.</span></span>                                   |
| <span data-ttu-id="74862-174">Win: suspender</span><span class="sxs-lookup"><span data-stu-id="74862-174">win:Suspend</span></span>   | <span data-ttu-id="74862-175">8</span><span class="sxs-lookup"><span data-stu-id="74862-175">8</span></span>     | <span data-ttu-id="74862-176">\_suspender código de operación WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="74862-176">WINEVENT\_OPCODE\_SUSPEND</span></span>   | <span data-ttu-id="74862-177">Evento que representa la actividad que se va a suspender pendiente de la finalización de otra actividad.</span><span class="sxs-lookup"><span data-stu-id="74862-177">An event that represents the activity being suspended pending another activity's completion.</span></span>           |
| <span data-ttu-id="74862-178">Win: enviar</span><span class="sxs-lookup"><span data-stu-id="74862-178">win:Send</span></span>      | <span data-ttu-id="74862-179">9</span><span class="sxs-lookup"><span data-stu-id="74862-179">9</span></span>     | <span data-ttu-id="74862-180">WINEVENT \_ envío de código de operación \_</span><span class="sxs-lookup"><span data-stu-id="74862-180">WINEVENT\_OPCODE\_SEND</span></span>      | <span data-ttu-id="74862-181">Evento que representa la transferencia de la actividad a otro componente.</span><span class="sxs-lookup"><span data-stu-id="74862-181">An event that represents transferring activity to another component.</span></span>                                   |
| <span data-ttu-id="74862-182">Win: Receive</span><span class="sxs-lookup"><span data-stu-id="74862-182">win:Receive</span></span>   | <span data-ttu-id="74862-183">240</span><span class="sxs-lookup"><span data-stu-id="74862-183">240</span></span>   | <span data-ttu-id="74862-184">WINEVENT de \_ código de operación \_ recibida</span><span class="sxs-lookup"><span data-stu-id="74862-184">WINEVENT\_OPCODE\_RECEIVE</span></span>   | <span data-ttu-id="74862-185">Evento que representa la recepción de una transferencia de actividad desde otro componente.</span><span class="sxs-lookup"><span data-stu-id="74862-185">An event that represents receiving an activity transfer from another component.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="74862-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74862-186">Requirements</span></span>



| <span data-ttu-id="74862-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="74862-187">Requirement</span></span> | <span data-ttu-id="74862-188">Value</span><span class="sxs-lookup"><span data-stu-id="74862-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74862-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74862-189">Minimum supported client</span></span><br/> | <span data-ttu-id="74862-190">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="74862-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74862-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74862-191">Minimum supported server</span></span><br/> | <span data-ttu-id="74862-192">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="74862-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





