---
description: Define una estructura que contiene uno o más valores de contador.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: struct (tipo complejo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667272"
---
# <a name="struct-complex-type"></a><span data-ttu-id="8cc5e-103">struct (tipo complejo)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-103">struct Complex Type</span></span>

<span data-ttu-id="8cc5e-104">Define una estructura que contiene uno o más valores de contador.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-104">Defines a structure that contains one or more counter values.</span></span>

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="8cc5e-105">Atributos</span><span class="sxs-lookup"><span data-stu-id="8cc5e-105">Attributes</span></span>



| <span data-ttu-id="8cc5e-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="8cc5e-106">Name</span></span> | <span data-ttu-id="8cc5e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="8cc5e-107">Type</span></span>                                                                    | <span data-ttu-id="8cc5e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cc5e-108">Description</span></span>                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc5e-109">name</span><span class="sxs-lookup"><span data-stu-id="8cc5e-109">name</span></span> | [<span data-ttu-id="8cc5e-110">**Man: CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="8cc5e-110">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="8cc5e-111">Nombre de la estructura.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-111">The name of the structure.</span></span><br/>                                                                                                            |
| <span data-ttu-id="8cc5e-112">type</span><span class="sxs-lookup"><span data-stu-id="8cc5e-112">type</span></span> | [<span data-ttu-id="8cc5e-113">**Man: CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="8cc5e-113">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="8cc5e-114">Nombre simbólico que identifica la estructura.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-114">A symbolic name that identifies the structure.</span></span> <span data-ttu-id="8cc5e-115">La herramienta [CTRPP](ctrpp.md) crea una variable de estructura con este nombre que puede usar.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-115">The [CTRPP](ctrpp.md) tool creates a struct variable with this name that you can use.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8cc5e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc5e-116">Requirements</span></span>



| <span data-ttu-id="8cc5e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc5e-117">Requirement</span></span> | <span data-ttu-id="8cc5e-118">Value</span><span class="sxs-lookup"><span data-stu-id="8cc5e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8cc5e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cc5e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc5e-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8cc5e-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8cc5e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cc5e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc5e-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8cc5e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




