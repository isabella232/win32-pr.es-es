---
title: Tipo complejo de StructDefinitionType
description: Define una estructura que incluye uno o más elementos de datos que desea incluir con el evento. | Tipo complejo de StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- StructDefinitionType tipo complejo EventLog
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698081"
---
# <a name="structdefinitiontype-complex-type"></a><span data-ttu-id="5e41d-105">Tipo complejo de StructDefinitionType</span><span class="sxs-lookup"><span data-stu-id="5e41d-105">StructDefinitionType Complex Type</span></span>

<span data-ttu-id="5e41d-106">Define una estructura que incluye uno o más elementos de datos que desea incluir con el evento.</span><span class="sxs-lookup"><span data-stu-id="5e41d-106">Defines a structure that includes one or more data items that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5e41d-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5e41d-107">Child elements</span></span>



| <span data-ttu-id="5e41d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e41d-108">Element</span></span>                                                               | <span data-ttu-id="5e41d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e41d-109">Type</span></span>                                                                             | <span data-ttu-id="5e41d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e41d-110">Description</span></span>                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="5e41d-111">**datos**</span><span class="sxs-lookup"><span data-stu-id="5e41d-111">**data**</span></span>](eventmanifestschema-data-structdefinitiontype-element.md) | [<span data-ttu-id="5e41d-112">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="5e41d-112">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md) | <span data-ttu-id="5e41d-113">Define un elemento de datos que desea incluir en la estructura.</span><span class="sxs-lookup"><span data-stu-id="5e41d-113">Defines a data item that you want to include in the structure.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="5e41d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e41d-114">Attributes</span></span>



| <span data-ttu-id="5e41d-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="5e41d-115">Name</span></span>   | <span data-ttu-id="5e41d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e41d-116">Type</span></span>                                                            | <span data-ttu-id="5e41d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e41d-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e41d-118">count</span><span class="sxs-lookup"><span data-stu-id="5e41d-118">count</span></span>  | [<span data-ttu-id="5e41d-119">**CountType**</span><span class="sxs-lookup"><span data-stu-id="5e41d-119">**CountType**</span></span>](eventmanifestschema-counttype-simpletype.md)   | <span data-ttu-id="5e41d-120">Número de elementos de una matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="5e41d-120">The number of elements in an array of structures.</span></span> <span data-ttu-id="5e41d-121">Este atributo indica que la estructura está definiendo una matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="5e41d-121">This attribute indicates that the structure is defining an array of structures.</span></span> <span data-ttu-id="5e41d-122">Puede especificar el recuento real o el nombre de un elemento de datos fuera de la estructura que contiene el recuento.</span><span class="sxs-lookup"><span data-stu-id="5e41d-122">You can specify the actual count or the name of a data item outside of the structure that contains the count.</span></span> <br/>                               |
| <span data-ttu-id="5e41d-123">length</span><span class="sxs-lookup"><span data-stu-id="5e41d-123">length</span></span> | [<span data-ttu-id="5e41d-124">**LengthType**</span><span class="sxs-lookup"><span data-stu-id="5e41d-124">**LengthType**</span></span>](eventmanifestschema-lengthtype-simpletype.md) | <span data-ttu-id="5e41d-125">No disponible.</span><span class="sxs-lookup"><span data-stu-id="5e41d-125">Not available.</span></span><br/> <span data-ttu-id="5e41d-126">**Windows Server 2008 y Windows Vista:** Longitud de esta estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="5e41d-126">**Windows Server 2008 and Windows Vista:** The length of this structure, in bytes.</span></span> <span data-ttu-id="5e41d-127">No está disponible a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e41d-127">Not available starting with Windows 7.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="5e41d-128">name</span><span class="sxs-lookup"><span data-stu-id="5e41d-128">name</span></span>   | <span data-ttu-id="5e41d-129">string</span><span class="sxs-lookup"><span data-stu-id="5e41d-129">string</span></span>                                                          | <span data-ttu-id="5e41d-130">Nombre de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5e41d-130">The name to the structure.</span></span> <span data-ttu-id="5e41d-131">Puede usar el nombre para hacer referencia al elemento de datos en el fragmento XML si especifica una sección [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5e41d-131">You can use the name to reference the data item in your XML fragment if you specify a [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) section in your template.</span></span><br/> <span data-ttu-id="5e41d-132">**Windows Vista:** Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="5e41d-132">**Windows Vista:** This attribute is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5e41d-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e41d-133">Remarks</span></span>

<span data-ttu-id="5e41d-134">Los proveedores escriben la estructura como un BLOB y no como miembros individuales de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5e41d-134">Providers write the structure as a blob and not as individual members of the structure.</span></span> <span data-ttu-id="5e41d-135">Si la estructura de C que está escribiendo contiene punteros (por ejemplo, un puntero de tipo LPWSTR), los datos del evento contendrán el valor del puntero, no los datos desreferenciados.</span><span class="sxs-lookup"><span data-stu-id="5e41d-135">If the C structure that you are writing contains pointers (for example, a pointer of type LPWSTR), the event data will contain the pointer value, not the dereferenced data.</span></span>

<span data-ttu-id="5e41d-136">No debe usar estructuras, sino que debe definir elementos de datos para cada miembro y escribirlos por separado.</span><span class="sxs-lookup"><span data-stu-id="5e41d-136">You should not use structures but instead should define data items for each member and write them separately.</span></span> <span data-ttu-id="5e41d-137">Si decide utilizar la estructura, la estructura solo debe contener tipos enteros y debe asegurarse de que los miembros de la estructura se alineen con un límite de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="5e41d-137">If you decide to use structure, the structure should contain only integral types and you must ensure that the members of the structure align to an 8-byte boundary.</span></span> <span data-ttu-id="5e41d-138">Si no lo hace, es probable que reciba errores de alineación cuando intente obtener acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="5e41d-138">If you do not, you will likely receive alignment errors when you try to access the data.</span></span> <span data-ttu-id="5e41d-139">Considere la posibilidad de usar la \# Directiva pragma Pack () para forzar la alineación en un límite de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="5e41d-139">Consider using the \#pragma pack() directive to force alignment on an 8-byte boundary.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e41d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e41d-140">Requirements</span></span>



| <span data-ttu-id="5e41d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e41d-141">Requirement</span></span> | <span data-ttu-id="5e41d-142">Value</span><span class="sxs-lookup"><span data-stu-id="5e41d-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e41d-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e41d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5e41d-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e41d-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e41d-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e41d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5e41d-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e41d-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





