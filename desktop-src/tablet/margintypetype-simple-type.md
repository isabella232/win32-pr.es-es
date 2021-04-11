---
description: Define el tipo que contiene los valores válidos para el atributo de tipo para el elemento margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Tipo simple de MarginTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278850"
---
# <a name="margintypetype-simple-type"></a><span data-ttu-id="a5672-103">Tipo simple de MarginTypeType</span><span class="sxs-lookup"><span data-stu-id="a5672-103">MarginTypeType Simple Type</span></span>

<span data-ttu-id="a5672-104">Define el tipo que contiene los valores válidos para el atributo de **tipo** para el [elemento margin](margin-element.md).</span><span class="sxs-lookup"><span data-stu-id="a5672-104">Defines the type that contains valid values for the **Type** attribute for the [Margin element](margin-element.md).</span></span>

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="a5672-105">Patrones</span><span class="sxs-lookup"><span data-stu-id="a5672-105">Patterns</span></span>

<span data-ttu-id="a5672-106">El tipo simple **MarginTypeType** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="a5672-106">The **MarginTypeType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `Left|Right`

## <a name="remarks"></a><span data-ttu-id="a5672-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5672-107">Remarks</span></span>

<span data-ttu-id="a5672-108">Los valores válidos para el atributo **Type** del [elemento margin](margin-element.md) son "left" y "Right".</span><span class="sxs-lookup"><span data-stu-id="a5672-108">The valid values for the **Type** attribute for the [Margin element](margin-element.md) are "Left" and "Right".</span></span>

## <a name="requirements"></a><span data-ttu-id="a5672-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5672-109">Requirements</span></span>



| <span data-ttu-id="a5672-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5672-110">Requirement</span></span> | <span data-ttu-id="a5672-111">Value</span><span class="sxs-lookup"><span data-stu-id="a5672-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a5672-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5672-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a5672-113">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a5672-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a5672-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5672-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a5672-115">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a5672-115">None supported</span></span><br/>                                     |



 

 




