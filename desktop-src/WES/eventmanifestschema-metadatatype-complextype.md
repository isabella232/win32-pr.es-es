---
title: Tipo complejo de MetadataType
description: Define los tipos de metadatos que puede definir en la sección de metadatos del manifiesto.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- MetadataType tipo complejo EventLog
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079729"
---
# <a name="metadatatype-complex-type"></a><span data-ttu-id="8f3e1-104">Tipo complejo de MetadataType</span><span class="sxs-lookup"><span data-stu-id="8f3e1-104">MetadataType Complex Type</span></span>

<span data-ttu-id="8f3e1-105">Define los tipos de metadatos que puede definir en la sección de metadatos del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-105">Defines the metadata types that you can define in the metadata section of the manifest.</span></span>

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8f3e1-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8f3e1-106">Child elements</span></span>



| <span data-ttu-id="8f3e1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8f3e1-107">Element</span></span>                                                                       | <span data-ttu-id="8f3e1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f3e1-108">Type</span></span>                                                                       | <span data-ttu-id="8f3e1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f3e1-109">Description</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f3e1-110">**circuitos**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-110">**channels**</span></span>](eventmanifestschema-channels-metadatatype-element.md)         | [<span data-ttu-id="8f3e1-111">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-111">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md) | <span data-ttu-id="8f3e1-112">Define una lista de canales en los que los proveedores pueden registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-112">Defines a list of channels to which providers can log events.</span></span> <span data-ttu-id="8f3e1-113">Después, un proveedor puede importar uno o varios de los canales en su manifiesto.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-113">A provider can then import one or more of the channels in their manifest.</span></span><br/>               |
| [<span data-ttu-id="8f3e1-114">**palabra**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-114">**keywords**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)         | [<span data-ttu-id="8f3e1-115">**KeywordListType**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-115">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md) | <span data-ttu-id="8f3e1-116">Define una lista de palabras clave que determinan la categoría de eventos que escribe el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-116">Defines a list of keywords that determine the category of events that the provider writes.</span></span><br/>                                                            |
| [<span data-ttu-id="8f3e1-117">**niveles**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-117">**levels**</span></span>](eventmanifestschema-levels-metadatatype-element.md)             | [<span data-ttu-id="8f3e1-118">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-118">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)     | <span data-ttu-id="8f3e1-119">Define una lista de niveles que especifican la gravedad de un evento.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-119">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                       |
| <span data-ttu-id="8f3e1-120">**message**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-120">**message**</span></span>                                                                   |                                                                            | <span data-ttu-id="8f3e1-121">Define una cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-121">Defines a message string.</span></span><br/>                                                                                                                             |
| <span data-ttu-id="8f3e1-122">**messageTable**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-122">**messageTable**</span></span>                                                              |                                                                            | <span data-ttu-id="8f3e1-123">Define una lista de cadenas de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-123">Defines a list of message strings.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="8f3e1-124">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-124">**namedQueries**</span></span>](eventmanifestschema-namedqueries-metadatatype-element.md) | [<span data-ttu-id="8f3e1-125">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-125">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)   | <span data-ttu-id="8f3e1-126">Define una lista de consultas con nombre que usan expresiones regulares para realizar acciones de búsqueda y reemplazo en la cadena de mensaje de un evento.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-126">Defines a list of named queries that use regular expressions to perform find and replace actions on an event's message string.</span></span><br/>                        |
| [<span data-ttu-id="8f3e1-127">**códigos**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-127">**opcodes**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)           | [<span data-ttu-id="8f3e1-128">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-128">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)   | <span data-ttu-id="8f3e1-129">Define una lista de códigos de tareas que se pueden usar para agrupar eventos dentro de una tarea.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-129">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                             |
| <span data-ttu-id="8f3e1-130">**tasks**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-130">**tasks**</span></span>                                                                     | [<span data-ttu-id="8f3e1-131">**TaskListType**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-131">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)       | <span data-ttu-id="8f3e1-132">Define una lista de tareas que un proveedor puede usar para agrupar los eventos.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-132">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="8f3e1-133">Normalmente, se usan tareas para agrupar los eventos de una característica o componente del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-133">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/> |
| [<span data-ttu-id="8f3e1-134">**distintos**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-134">**types**</span></span>](eventmanifestschema-types-metadatatype-element.md)               | [<span data-ttu-id="8f3e1-135">**TypeListType**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-135">**TypeListType**</span></span>](eventmanifestschema-typelisttype-complextype.md)       | <span data-ttu-id="8f3e1-136">Define una lista de tipos XML.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-136">Defines a list of XML types.</span></span><br/>                                                                                                                          |



## <a name="attributes"></a><span data-ttu-id="8f3e1-137">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f3e1-137">Attributes</span></span>



| <span data-ttu-id="8f3e1-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f3e1-138">Name</span></span>    | <span data-ttu-id="8f3e1-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f3e1-139">Type</span></span>                                                              | <span data-ttu-id="8f3e1-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f3e1-140">Description</span></span>                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3e1-141">message</span><span class="sxs-lookup"><span data-stu-id="8f3e1-141">message</span></span> | [<span data-ttu-id="8f3e1-142">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-142">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="8f3e1-143">Referencia a la cadena localizada en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-143">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="8f3e1-144">mId</span><span class="sxs-lookup"><span data-stu-id="8f3e1-144">mid</span></span>     | <span data-ttu-id="8f3e1-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="8f3e1-145">xs:string</span></span>                                                         | <span data-ttu-id="8f3e1-146">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-146">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="8f3e1-147">name</span><span class="sxs-lookup"><span data-stu-id="8f3e1-147">name</span></span>    | <span data-ttu-id="8f3e1-148">anyURI</span><span class="sxs-lookup"><span data-stu-id="8f3e1-148">anyURI</span></span>                                                            | <span data-ttu-id="8f3e1-149">URI del archivo meta.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-149">The URI of the meta file.</span></span> <br/>                                                              |
| <span data-ttu-id="8f3e1-150">símbolo</span><span class="sxs-lookup"><span data-stu-id="8f3e1-150">symbol</span></span>  | [<span data-ttu-id="8f3e1-151">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-151">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="8f3e1-152">Nombre simbólico que desea que cree el compilador de mensajes para esta cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-152">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="8f3e1-153">value</span><span class="sxs-lookup"><span data-stu-id="8f3e1-153">value</span></span>   | [<span data-ttu-id="8f3e1-154">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="8f3e1-154">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="8f3e1-155">Número que se va a usar como identificador de mensaje para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-155">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="remarks"></a><span data-ttu-id="8f3e1-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f3e1-156">Remarks</span></span>

<span data-ttu-id="8f3e1-157">Aunque puede crear un manifiesto que contiene una sección de metadatos, el servicio no lo usará; los únicos metadatos que reconoce el servicio son los metadatos que se encuentran en el archivo de Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="8f3e1-157">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3e1-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f3e1-158">Requirements</span></span>



| <span data-ttu-id="8f3e1-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3e1-159">Requirement</span></span> | <span data-ttu-id="8f3e1-160">Value</span><span class="sxs-lookup"><span data-stu-id="8f3e1-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f3e1-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f3e1-161">Minimum supported client</span></span><br/> | <span data-ttu-id="8f3e1-162">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8f3e1-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8f3e1-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f3e1-163">Minimum supported server</span></span><br/> | <span data-ttu-id="8f3e1-164">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f3e1-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





