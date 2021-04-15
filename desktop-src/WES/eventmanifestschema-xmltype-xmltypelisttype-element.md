---
title: Elemento xmlType (XmlTypeListType)
description: Define un tipo XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- elemento xmlType EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695918"
---
# <a name="xmltype-xmltypelisttype-element"></a><span data-ttu-id="9942c-104">Elemento xmlType (XmlTypeListType)</span><span class="sxs-lookup"><span data-stu-id="9942c-104">xmlType (XmlTypeListType) Element</span></span>

<span data-ttu-id="9942c-105">Define un tipo XML.</span><span class="sxs-lookup"><span data-stu-id="9942c-105">Defines an XML type.</span></span>

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="9942c-106">El elemento **xmlType** se define mediante el tipo complejo de [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9942c-106">The **xmlType** element is defined by the [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="9942c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="9942c-107">Attributes</span></span>



| <span data-ttu-id="9942c-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="9942c-108">Name</span></span>   | <span data-ttu-id="9942c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9942c-109">Type</span></span>      | <span data-ttu-id="9942c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9942c-110">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9942c-111">name</span><span class="sxs-lookup"><span data-stu-id="9942c-111">name</span></span>   | <span data-ttu-id="9942c-112">**QName**</span><span class="sxs-lookup"><span data-stu-id="9942c-112">**QName**</span></span> | <span data-ttu-id="9942c-113">Nombre del tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="9942c-113">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="9942c-114">símbolo</span><span class="sxs-lookup"><span data-stu-id="9942c-114">symbol</span></span> | <span data-ttu-id="9942c-115">string</span><span class="sxs-lookup"><span data-stu-id="9942c-115">string</span></span>    | <span data-ttu-id="9942c-116">Símbolo que se va a usar para hacer referencia al tipo de salida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9942c-116">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="9942c-117">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el tipo de salida en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="9942c-117">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="9942c-118">value</span><span class="sxs-lookup"><span data-stu-id="9942c-118">value</span></span>  | <span data-ttu-id="9942c-119">string</span><span class="sxs-lookup"><span data-stu-id="9942c-119">string</span></span>    | <span data-ttu-id="9942c-120">Valor entero que identifica de forma única el tipo de salida en la lista de tipos de salida que se define.</span><span class="sxs-lookup"><span data-stu-id="9942c-120">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="9942c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9942c-121">Requirements</span></span>



| <span data-ttu-id="9942c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9942c-122">Requirement</span></span> | <span data-ttu-id="9942c-123">Value</span><span class="sxs-lookup"><span data-stu-id="9942c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9942c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9942c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9942c-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9942c-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9942c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9942c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9942c-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9942c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9942c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9942c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9942c-129">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="9942c-129">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="9942c-130">**xmlTypes (TypeListType)**</span><span class="sxs-lookup"><span data-stu-id="9942c-130">**xmlTypes (TypeListType)**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





