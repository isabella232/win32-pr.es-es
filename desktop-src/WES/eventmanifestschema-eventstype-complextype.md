---
title: Tipo complejo de EventsType
description: Contiene una lista de proveedores definidos en el manifiesto. | Tipo complejo de EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventsType tipo complejo EventLog
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698100"
---
# <a name="eventstype-complex-type"></a><span data-ttu-id="e6df3-105">Tipo complejo de EventsType</span><span class="sxs-lookup"><span data-stu-id="e6df3-105">EventsType Complex Type</span></span>

<span data-ttu-id="e6df3-106">Contiene una lista de proveedores definidos en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="e6df3-106">Contains a list of providers that are defined in the manifest.</span></span>

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e6df3-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6df3-107">Child elements</span></span>

| <span data-ttu-id="e6df3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e6df3-108">Element</span></span> | <span data-ttu-id="e6df3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6df3-109">Type</span></span> | <span data-ttu-id="e6df3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6df3-110">Description</span></span> |
|---------|------|-------------|
| <span data-ttu-id="e6df3-111">message</span><span class="sxs-lookup"><span data-stu-id="e6df3-111">message</span></span> |      | <span data-ttu-id="e6df3-112">Define una cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6df3-112">Defines a message string.</span></span> |
| <span data-ttu-id="e6df3-113">messageTable</span><span class="sxs-lookup"><span data-stu-id="e6df3-113">messageTable</span></span> | | <span data-ttu-id="e6df3-114">Define una lista de cadenas de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6df3-114">Defines a list of message strings.</span></span> <span data-ttu-id="e6df3-115">No debe tener que utilizar una tabla de mensajes excepto en los casos siguientes, donde debe definir una tabla de mensajes para asignar explícitamente los números de recursos a las cadenas de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6df3-115">You should not have to use a message table except in the following cases where you must define a message table to explicitly assign resource numbers to message strings.</span></span> <ul><li><span data-ttu-id="e6df3-116">Está migrando desde un archivo de texto de mensaje (. MC) a un manifiesto, pero sigue escribiendo eventos en los canales del sistema y de la aplicación, para que los consumidores heredados sigan consumiendo los eventos.</span><span class="sxs-lookup"><span data-stu-id="e6df3-116">You are migrating from a message text (.mc) file to a manifest but are still writing events to the application and system channels, so that legacy consumers to continue consuming the events.</span></span> <span data-ttu-id="e6df3-117">Para realizar este trabajo, los identificadores de recursos para las cadenas de mensaje definidas en el manifiesto deben ser los mismos que los identificadores de eventos.</span><span class="sxs-lookup"><span data-stu-id="e6df3-117">To make this work, the resource identifiers for the message strings defined in the manifest must be the same as the event identifiers.</span></span> <span data-ttu-id="e6df3-118">Sin embargo, el compilador de mensajes asigna automáticamente identificadores de recursos a las cadenas de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6df3-118">However, the message compiler automatically assigns resource identifiers to the message strings.</span></span> <span data-ttu-id="e6df3-119">Para invalidar el compilador, utilice la tabla de mensajes y establezca el atributo de valor en el identificador de eventos y el atributo de mensaje para hacer referencia a una cadena en la tabla de cadenas en la sección de localización del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="e6df3-119">To override the compiler, use the message table and set the value attribute to the event identifier and the message attribute to refer to a string in the string table in the localization section of the manifest.</span></span></li><li><span data-ttu-id="e6df3-120">Si desea identificar más de 16 proveedores, debe incluir la tabla de mensajes que los proveedores decimoséptima y on deben usar para asignar valores de recursos para las cadenas de mensaje que definen.</span><span class="sxs-lookup"><span data-stu-id="e6df3-120">If you want to identify more than 16 providers, you must include the message table that the seventeenth and on providers must use to assign resource values for the message strings that they define.</span></span> <span data-ttu-id="e6df3-121">Si el proveedor hace referencia a cadenas de mensaje que se definen entre el 1 y el 16, no se incluyen esas cadenas de mensaje en la tabla de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e6df3-121">If the provider references message strings that providers 1 through 16 defined, you do not include those message strings in the message table.</span></span></li></ul>|
| [<span data-ttu-id="e6df3-122">**presta**</span><span class="sxs-lookup"><span data-stu-id="e6df3-122">**provider**</span></span>](eventmanifestschema-provider-eventstype-element.md) | [<span data-ttu-id="e6df3-123">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="e6df3-123">**ProviderType**</span></span>](eventmanifestschema-providertype-complextype.md) | <span data-ttu-id="e6df3-124">Una lista de proveedores que desea definir.</span><span class="sxs-lookup"><span data-stu-id="e6df3-124">A list of providers that you want to define.</span></span> |

## <a name="attributes"></a><span data-ttu-id="e6df3-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6df3-125">Attributes</span></span>

| <span data-ttu-id="e6df3-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6df3-126">Name</span></span>    | <span data-ttu-id="e6df3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6df3-127">Type</span></span>                                                             | <span data-ttu-id="e6df3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6df3-128">Description</span></span>                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6df3-129">message</span><span class="sxs-lookup"><span data-stu-id="e6df3-129">message</span></span> | [<span data-ttu-id="e6df3-130">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="e6df3-130">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="e6df3-131">Referencia a la cadena localizada en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="e6df3-131">A reference to the localized string in the string table.</span></span>                               |
| <span data-ttu-id="e6df3-132">mId</span><span class="sxs-lookup"><span data-stu-id="e6df3-132">mid</span></span>     | <span data-ttu-id="e6df3-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6df3-133">xs:string</span></span>                                                        | <span data-ttu-id="e6df3-134">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e6df3-134">Not used.</span></span>                                                                              |
| <span data-ttu-id="e6df3-135">símbolo</span><span class="sxs-lookup"><span data-stu-id="e6df3-135">symbol</span></span>  | [<span data-ttu-id="e6df3-136">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="e6df3-136">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="e6df3-137">Nombre simbólico que desea que cree el compilador de mensajes para esta cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6df3-137">The symbolic name that you want the message compiler to create for this message string.</span></span>|
| <span data-ttu-id="e6df3-138">value</span><span class="sxs-lookup"><span data-stu-id="e6df3-138">value</span></span>   | [<span data-ttu-id="e6df3-139">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="e6df3-139">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="e6df3-140">Número que se va a usar como identificador de mensaje para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6df3-140">The number to use as the message identifier for this message.</span></span>                          |


## <a name="remarks"></a><span data-ttu-id="e6df3-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6df3-141">Remarks</span></span>

<span data-ttu-id="e6df3-142">El límite práctico del número de proveedores que puede definir en un manifiesto es de 16 proveedores.</span><span class="sxs-lookup"><span data-stu-id="e6df3-142">The practical limit of the number of providers that you can define in a manifest is 16 providers.</span></span> <span data-ttu-id="e6df3-143">Si especifica más de 16 proveedores, debe usar una tabla de mensajes para asignar explícitamente los números de recursos a las cadenas de mensaje a las que hace referencia el proveedor.</span><span class="sxs-lookup"><span data-stu-id="e6df3-143">If you specify more than 16 providers, you must use a message table to explicitly assign resource numbers to the message strings that the provider references.</span></span> <span data-ttu-id="e6df3-144">Para obtener más información, vea el elemento message anterior.</span><span class="sxs-lookup"><span data-stu-id="e6df3-144">For more details, see the message element above.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6df3-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6df3-145">Requirements</span></span>

| <span data-ttu-id="e6df3-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6df3-146">Requirement</span></span> | <span data-ttu-id="e6df3-147">Value</span><span class="sxs-lookup"><span data-stu-id="e6df3-147">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="e6df3-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6df3-148">Minimum supported client</span></span> | <span data-ttu-id="e6df3-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e6df3-149">Windows Vista \[desktop apps only\]</span></span>       |
| <span data-ttu-id="e6df3-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6df3-150">Minimum supported server</span></span> | <span data-ttu-id="e6df3-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6df3-151">Windows Server 2008 \[desktop apps only\]</span></span> |
