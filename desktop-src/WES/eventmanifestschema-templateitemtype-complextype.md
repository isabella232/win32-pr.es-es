---
title: Tipo complejo de TemplateItemType
description: Plantilla que define los datos que se van a incluir con un evento. | Tipo complejo de TemplateItemType
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- TemplateItemType tipo complejo EventLog
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280076"
---
# <a name="templateitemtype-complex-type"></a><span data-ttu-id="4c5fc-105">Tipo complejo de TemplateItemType</span><span class="sxs-lookup"><span data-stu-id="4c5fc-105">TemplateItemType Complex Type</span></span>

<span data-ttu-id="4c5fc-106">Plantilla que define los datos que se van a incluir con un evento.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-106">A template that defines the data to include with an event.</span></span>

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4c5fc-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c5fc-107">Child elements</span></span>



| <span data-ttu-id="4c5fc-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4c5fc-108">Element</span></span>                                                                   | <span data-ttu-id="4c5fc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c5fc-109">Type</span></span>                                                                                 | <span data-ttu-id="4c5fc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c5fc-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c5fc-111">**binario**</span><span class="sxs-lookup"><span data-stu-id="4c5fc-111">**binary**</span></span>](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | <span data-ttu-id="4c5fc-112">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-112">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="4c5fc-113">**datos**</span><span class="sxs-lookup"><span data-stu-id="4c5fc-113">**data**</span></span>](eventmanifestschema-data-templateitemtype-element.md)         | [<span data-ttu-id="4c5fc-114">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="4c5fc-114">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md)     | <span data-ttu-id="4c5fc-115">Define un elemento de datos que desea incluir con el evento.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-115">Defines a data item that you want to include with the event.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="4c5fc-116">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="4c5fc-116">**struct**</span></span>](eventmanifestschema-struct-templateitemtype-element.md)     | [<span data-ttu-id="4c5fc-117">**StructDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="4c5fc-117">**StructDefinitionType**</span></span>](eventmanifestschema-structdefinitiontype-complextype.md) | <span data-ttu-id="4c5fc-118">Define una estructura que incluye uno o más elementos de datos que desea incluir con el evento.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-118">Defines a structure that includes one or more data items that you want to include with the event.</span></span> <span data-ttu-id="4c5fc-119">Los proveedores escriben la estructura como un BLOB y no como miembros individuales de la estructura.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-119">Providers write the structure as a blob and not as individual members of the structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="4c5fc-120">**UserData**</span><span class="sxs-lookup"><span data-stu-id="4c5fc-120">**UserData**</span></span>](eventmanifestschema-userdata-templateitemtype-element.md) | [<span data-ttu-id="4c5fc-121">**XmlType**</span><span class="sxs-lookup"><span data-stu-id="4c5fc-121">**XmlType**</span></span>](eventmanifestschema-xmltype-complextype.md)                           | <span data-ttu-id="4c5fc-122">Fragmento XML que se utiliza para representar los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-122">An XML fragment that is used to render the event data.</span></span> <span data-ttu-id="4c5fc-123">Si no incluye el fragmento, los datos de evento se representan en el orden en que los elementos de datos se definen en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-123">If you do not include the fragment, the event data is rendered in the order that the data items are defined in the template.</span></span> <span data-ttu-id="4c5fc-124">El contenido de este elemento es cualquier fragmento XML válido.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-124">The contents of this element is any valid XML fragment.</span></span> <span data-ttu-id="4c5fc-125">El fragmento debe contener solo un nodo de nivel superior y el nodo de nivel superior debe especificar su propio espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-125">The fragment must contain only one top-level node and the top-level node must specify its own namespace.</span></span> <br/> <span data-ttu-id="4c5fc-126">Para hacer referencia a un elemento de datos del fragmento, establezca el cuerpo del texto de un nodo del fragmento en%*n*, donde *n* es el índice basado en uno de los elementos de datos de nivel superior de la lista de elementos de datos (no se puede hacer referencia a los miembros de una estructura).</span><span class="sxs-lookup"><span data-stu-id="4c5fc-126">To reference a data item in the fragment, set the text body for a node in the fragment to %*n*, where *n* is the one-based index of the top-level data items in the list of data items (you cannot reference members of a structure).</span></span> <span data-ttu-id="4c5fc-127">El valor de índice que especifique no debe ser mayor que el número de elementos de datos de nivel superior de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-127">The index value that you specify must not be greater than the number of top-level data items in the template.</span></span><br/> <span data-ttu-id="4c5fc-128">Este elemento sigue a todos los **datos** y elementos de **estructura** .</span><span class="sxs-lookup"><span data-stu-id="4c5fc-128">This element follows all **data** and **struct** elements.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="4c5fc-129">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c5fc-129">Attributes</span></span>



| <span data-ttu-id="4c5fc-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="4c5fc-130">Name</span></span> | <span data-ttu-id="4c5fc-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c5fc-131">Type</span></span>   | <span data-ttu-id="4c5fc-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c5fc-132">Description</span></span>                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5fc-133">name</span><span class="sxs-lookup"><span data-stu-id="4c5fc-133">name</span></span> | <span data-ttu-id="4c5fc-134">string</span><span class="sxs-lookup"><span data-stu-id="4c5fc-134">string</span></span> | <span data-ttu-id="4c5fc-135">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-135">Reserved for internal use only.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="4c5fc-136">name</span><span class="sxs-lookup"><span data-stu-id="4c5fc-136">name</span></span> | <span data-ttu-id="4c5fc-137">string</span><span class="sxs-lookup"><span data-stu-id="4c5fc-137">string</span></span> | <span data-ttu-id="4c5fc-138">Nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-138">The name of the template.</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="4c5fc-139">tid</span><span class="sxs-lookup"><span data-stu-id="4c5fc-139">tid</span></span>  | <span data-ttu-id="4c5fc-140">token</span><span class="sxs-lookup"><span data-stu-id="4c5fc-140">token</span></span>  | <span data-ttu-id="4c5fc-141">Identificador que identifica de forma única la plantilla en la lista de plantillas que define el proveedor.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-141">An identifier that uniquely identifies the template within the list of templates that the provider defines.</span></span> <span data-ttu-id="4c5fc-142">Use este nombre para hacer referencia a la plantilla al definir la definición del evento.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-142">Use this name to reference the template when you define your event definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4c5fc-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c5fc-143">Remarks</span></span>

<span data-ttu-id="4c5fc-144">La definición de plantilla debe tener al menos un elemento secundario de datos o struct.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-144">The template definition must have at least one data or struct child element.</span></span> <span data-ttu-id="4c5fc-145">El proveedor debe escribir los datos de evento en el orden de los elementos de datos definidos en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-145">The provider must write the event data in the order of the data items defined in the template.</span></span>

<span data-ttu-id="4c5fc-146">El tamaño de todos los elementos de datos de la plantilla debe ser inferior a 64 KB.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-146">The size of all the data items in the template must be less than 64 KB.</span></span>

## <a name="examples"></a><span data-ttu-id="4c5fc-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4c5fc-147">Examples</span></span>

<span data-ttu-id="4c5fc-148">En el ejemplo siguiente se muestra cómo crear una definición de plantilla.</span><span class="sxs-lookup"><span data-stu-id="4c5fc-148">The following example shows how to create a template definition.</span></span>


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a><span data-ttu-id="4c5fc-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c5fc-149">Requirements</span></span>



| <span data-ttu-id="4c5fc-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c5fc-150">Requirement</span></span> | <span data-ttu-id="4c5fc-151">Value</span><span class="sxs-lookup"><span data-stu-id="4c5fc-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c5fc-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c5fc-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5fc-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4c5fc-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c5fc-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c5fc-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5fc-155">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c5fc-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





