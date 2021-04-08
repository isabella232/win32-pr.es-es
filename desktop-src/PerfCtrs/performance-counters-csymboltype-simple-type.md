---
description: Define un nombre de símbolo de C/C++ válido.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo simple de CSymbolType (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001968"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="b94c5-103">Tipo simple de CSymbolType (contadores de rendimiento)</span><span class="sxs-lookup"><span data-stu-id="b94c5-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="b94c5-104">Define un nombre de símbolo de C/C++ válido.</span><span class="sxs-lookup"><span data-stu-id="b94c5-104">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="b94c5-105">Patrones</span><span class="sxs-lookup"><span data-stu-id="b94c5-105">Patterns</span></span>

<span data-ttu-id="b94c5-106">El tipo simple **CSymbolType** es **xs: String** , que está restringido por el patrón siguiente:</span><span class="sxs-lookup"><span data-stu-id="b94c5-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="b94c5-107">El nombre del símbolo puede estar vacío o contener caracteres alfanuméricos y caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="b94c5-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="b94c5-108">Si especifica un nombre, el nombre debe comenzar con un carácter de subrayado ( \_ ) o alfabético.</span><span class="sxs-lookup"><span data-stu-id="b94c5-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="b94c5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b94c5-109">Requirements</span></span>



| <span data-ttu-id="b94c5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b94c5-110">Requirement</span></span> | <span data-ttu-id="b94c5-111">Value</span><span class="sxs-lookup"><span data-stu-id="b94c5-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b94c5-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b94c5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b94c5-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b94c5-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b94c5-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b94c5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b94c5-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b94c5-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




