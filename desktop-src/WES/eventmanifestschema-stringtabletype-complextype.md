---
title: Tipo complejo de StringTableType
description: Define una lista de cadenas traducidas a las que se puede hacer referencia en el manifiesto. | Tipo complejo de StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- StringTableType tipo complejo EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698111"
---
# <a name="stringtabletype-complex-type"></a><span data-ttu-id="47163-105">Tipo complejo de StringTableType</span><span class="sxs-lookup"><span data-stu-id="47163-105">StringTableType Complex Type</span></span>

<span data-ttu-id="47163-106">Define una lista de cadenas traducidas a las que se puede hacer referencia en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="47163-106">Defines a list of localized strings that you can reference in your manifest.</span></span>

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="47163-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="47163-107">Child elements</span></span>



| <span data-ttu-id="47163-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="47163-108">Element</span></span>                                                              | <span data-ttu-id="47163-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="47163-109">Type</span></span> | <span data-ttu-id="47163-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="47163-110">Description</span></span>                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [<span data-ttu-id="47163-111">**string**</span><span class="sxs-lookup"><span data-stu-id="47163-111">**string**</span></span>](eventmanifestschema-string-stringtabletype-element.md) |      | <span data-ttu-id="47163-112">Define una cadena traducida.</span><span class="sxs-lookup"><span data-stu-id="47163-112">Defines a localized string.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="47163-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="47163-113">Attributes</span></span>



| <span data-ttu-id="47163-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="47163-114">Name</span></span>       | <span data-ttu-id="47163-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="47163-115">Type</span></span>   | <span data-ttu-id="47163-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="47163-116">Description</span></span>                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47163-117">id</span><span class="sxs-lookup"><span data-stu-id="47163-117">id</span></span>         | <span data-ttu-id="47163-118">string</span><span class="sxs-lookup"><span data-stu-id="47163-118">string</span></span> | <span data-ttu-id="47163-119">Identificador que identifica de forma única la cadena en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="47163-119">An identifier that uniquely identifies the string within the string table.</span></span> <span data-ttu-id="47163-120">Por ejemplo, "Printer. Connection".</span><span class="sxs-lookup"><span data-stu-id="47163-120">For example, "Printer.Connection".</span></span><br/> |
| <span data-ttu-id="47163-121">stringType</span><span class="sxs-lookup"><span data-stu-id="47163-121">stringType</span></span> | <span data-ttu-id="47163-122">string</span><span class="sxs-lookup"><span data-stu-id="47163-122">string</span></span> | <span data-ttu-id="47163-123">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="47163-123">Not used.</span></span><br/>                                                                                                     |
| <span data-ttu-id="47163-124">value</span><span class="sxs-lookup"><span data-stu-id="47163-124">value</span></span>      | <span data-ttu-id="47163-125">string</span><span class="sxs-lookup"><span data-stu-id="47163-125">string</span></span> | <span data-ttu-id="47163-126">Cadena localizada.</span><span class="sxs-lookup"><span data-stu-id="47163-126">The localized string.</span></span><br/>                                                                                         |



## <a name="remarks"></a><span data-ttu-id="47163-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47163-127">Remarks</span></span>

<span data-ttu-id="47163-128">Puede hacer referencia a las cadenas desde cualquier tipo de manifiesto que contenga el atributo Message.</span><span class="sxs-lookup"><span data-stu-id="47163-128">You can reference the strings from any manifest type that contains the message attribute.</span></span> <span data-ttu-id="47163-129">Para hacer referencia a una cadena con un valor de stringType de "String" y un identificador de "Printer. Connection", use $ (String. Printer. Connection) como valor del atributo Message.</span><span class="sxs-lookup"><span data-stu-id="47163-129">To reference a string with a stringType of "string" and an id of "Printer.Connection", use $(string.Printer.Connection) as the value of the message attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="47163-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47163-130">Requirements</span></span>



| <span data-ttu-id="47163-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="47163-131">Requirement</span></span> | <span data-ttu-id="47163-132">Value</span><span class="sxs-lookup"><span data-stu-id="47163-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="47163-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47163-133">Minimum supported client</span></span><br/> | <span data-ttu-id="47163-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="47163-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="47163-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47163-135">Minimum supported server</span></span><br/> | <span data-ttu-id="47163-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="47163-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





