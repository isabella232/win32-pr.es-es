---
title: Tipo complejo de XmlTypeListType
description: Define una lista de tipos de salida que el servicio usa para determinar cómo se representa un tipo de datos de entrada.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- XmlTypeListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359757"
---
# <a name="xmltypelisttype-complex-type"></a><span data-ttu-id="27dab-104">Tipo complejo de XmlTypeListType</span><span class="sxs-lookup"><span data-stu-id="27dab-104">XmlTypeListType Complex Type</span></span>

<span data-ttu-id="27dab-105">Define una lista de tipos de salida que el servicio usa para determinar cómo se representa un tipo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="27dab-105">Defines a list output types that the service uses to determine how to render an input data type.</span></span>

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
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
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="27dab-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="27dab-106">Child elements</span></span>



| <span data-ttu-id="27dab-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="27dab-107">Element</span></span>                                                                | <span data-ttu-id="27dab-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="27dab-108">Type</span></span> | <span data-ttu-id="27dab-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="27dab-109">Description</span></span>                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [<span data-ttu-id="27dab-110">**xmlType**</span><span class="sxs-lookup"><span data-stu-id="27dab-110">**xmlType**</span></span>](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | <span data-ttu-id="27dab-111">Define un tipo XML.</span><span class="sxs-lookup"><span data-stu-id="27dab-111">Defines an XML type.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="27dab-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="27dab-112">Attributes</span></span>



| <span data-ttu-id="27dab-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="27dab-113">Name</span></span>   | <span data-ttu-id="27dab-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="27dab-114">Type</span></span>                                                              | <span data-ttu-id="27dab-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="27dab-115">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27dab-116">name</span><span class="sxs-lookup"><span data-stu-id="27dab-116">name</span></span>   | <span data-ttu-id="27dab-117">**QName**</span><span class="sxs-lookup"><span data-stu-id="27dab-117">**QName**</span></span>                                                         | <span data-ttu-id="27dab-118">Nombre del tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="27dab-118">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="27dab-119">símbolo</span><span class="sxs-lookup"><span data-stu-id="27dab-119">symbol</span></span> | [<span data-ttu-id="27dab-120">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="27dab-120">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="27dab-121">Símbolo que se va a usar para hacer referencia al tipo de salida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27dab-121">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="27dab-122">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el tipo de salida en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="27dab-122">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="27dab-123">value</span><span class="sxs-lookup"><span data-stu-id="27dab-123">value</span></span>  | <span data-ttu-id="27dab-124">string</span><span class="sxs-lookup"><span data-stu-id="27dab-124">string</span></span>                                                            | <span data-ttu-id="27dab-125">Valor entero que identifica de forma única el tipo de salida en la lista de tipos de salida que se define.</span><span class="sxs-lookup"><span data-stu-id="27dab-125">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="27dab-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27dab-126">Remarks</span></span>

<span data-ttu-id="27dab-127">El \\ archivo de inclusión de \\Winmeta.xml, que se incluye en el Windows SDK, contiene una lista de tipos de salida predefinidos.</span><span class="sxs-lookup"><span data-stu-id="27dab-127">The \\Include\\Winmeta.xml file, which is included in the Windows SDK, contains a list of predefined output types.</span></span>

## <a name="requirements"></a><span data-ttu-id="27dab-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27dab-128">Requirements</span></span>



| <span data-ttu-id="27dab-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="27dab-129">Requirement</span></span> | <span data-ttu-id="27dab-130">Value</span><span class="sxs-lookup"><span data-stu-id="27dab-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27dab-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27dab-131">Minimum supported client</span></span><br/> | <span data-ttu-id="27dab-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="27dab-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="27dab-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27dab-133">Minimum supported server</span></span><br/> | <span data-ttu-id="27dab-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="27dab-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





