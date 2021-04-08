---
description: Define la sección del manifiesto de instrumentación que identifica el proveedor y los contadores que proporcionan.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Tipo complejo de contadores
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001969"
---
# <a name="counters-complex-type"></a><span data-ttu-id="0e9a6-103">Tipo complejo de contadores</span><span class="sxs-lookup"><span data-stu-id="0e9a6-103">counters Complex Type</span></span>

<span data-ttu-id="0e9a6-104">Define la sección del manifiesto de instrumentación que identifica el proveedor y los contadores que proporcionan.</span><span class="sxs-lookup"><span data-stu-id="0e9a6-104">Defines the section of the instrumentation manifest that identifies the provider and the counters that they provide.</span></span>

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0e9a6-105">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e9a6-105">Child elements</span></span>



| <span data-ttu-id="0e9a6-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0e9a6-106">Element</span></span>      | <span data-ttu-id="0e9a6-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e9a6-107">Type</span></span>                                                               | <span data-ttu-id="0e9a6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e9a6-108">Description</span></span>                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="0e9a6-109">**presta**</span><span class="sxs-lookup"><span data-stu-id="0e9a6-109">**provider**</span></span> | [<span data-ttu-id="0e9a6-110">**Man: proveedor**</span><span class="sxs-lookup"><span data-stu-id="0e9a6-110">**man:provider**</span></span>](performance-counters-provider-complex-type.md) | <span data-ttu-id="0e9a6-111">Identifica un proveedor que proporciona contadores.</span><span class="sxs-lookup"><span data-stu-id="0e9a6-111">Identifies a provider that provides counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0e9a6-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e9a6-112">Attributes</span></span>



| <span data-ttu-id="0e9a6-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="0e9a6-113">Name</span></span>          | <span data-ttu-id="0e9a6-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e9a6-114">Type</span></span> | <span data-ttu-id="0e9a6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e9a6-115">Description</span></span>                                                      |
|---------------|------|------------------------------------------------------------------|
| <span data-ttu-id="0e9a6-116">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="0e9a6-116">schemaVersion</span></span> |      | <span data-ttu-id="0e9a6-117">Versión del esquema que se usa para escribir el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="0e9a6-117">The version of the schema used to write the manifest.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0e9a6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e9a6-118">Requirements</span></span>



| <span data-ttu-id="0e9a6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e9a6-119">Requirement</span></span> | <span data-ttu-id="0e9a6-120">Value</span><span class="sxs-lookup"><span data-stu-id="0e9a6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e9a6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e9a6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9a6-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0e9a6-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e9a6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e9a6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9a6-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e9a6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e9a6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e9a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9a6-126">**instrumentación**</span><span class="sxs-lookup"><span data-stu-id="0e9a6-126">**instrumentation**</span></span>](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

