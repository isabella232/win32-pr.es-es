---
description: Define los valores válidos para el atributo de estilo del elemento LineLayout.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Tipo simple de LineLayoutStyleType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697756"
---
# <a name="linelayoutstyletype-simple-type"></a><span data-ttu-id="16869-103">Tipo simple de LineLayoutStyleType</span><span class="sxs-lookup"><span data-stu-id="16869-103">LineLayoutStyleType Simple Type</span></span>

<span data-ttu-id="16869-104">Define los valores válidos para el atributo de **estilo** del [elemento LineLayout](linelayout-element.md).</span><span class="sxs-lookup"><span data-stu-id="16869-104">Defines the valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md).</span></span>

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="16869-105">Patrones</span><span class="sxs-lookup"><span data-stu-id="16869-105">Patterns</span></span>

<span data-ttu-id="16869-106">El tipo simple **LineLayoutStyleType** es una cadena restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="16869-106">The **LineLayoutStyleType** simple type is a string that is restricted by the following pattern:</span></span>

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a><span data-ttu-id="16869-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16869-107">Remarks</span></span>

<span data-ttu-id="16869-108">Los valores válidos para el atributo de **estilo** del [elemento LineLayout](linelayout-element.md) son:</span><span class="sxs-lookup"><span data-stu-id="16869-108">Valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md) are:</span></span>

-   <span data-ttu-id="16869-109">None</span><span class="sxs-lookup"><span data-stu-id="16869-109">None</span></span>
-   <span data-ttu-id="16869-110">Sólido</span><span class="sxs-lookup"><span data-stu-id="16869-110">Solid</span></span>
-   <span data-ttu-id="16869-111">Guión</span><span class="sxs-lookup"><span data-stu-id="16869-111">Dash</span></span>
-   <span data-ttu-id="16869-112">Punto</span><span class="sxs-lookup"><span data-stu-id="16869-112">Dot</span></span>
-   <span data-ttu-id="16869-113">DashDot</span><span class="sxs-lookup"><span data-stu-id="16869-113">DashDot</span></span>
-   <span data-ttu-id="16869-114">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="16869-114">DashDotDot</span></span>
-   <span data-ttu-id="16869-115">Doble</span><span class="sxs-lookup"><span data-stu-id="16869-115">Double</span></span>

## <a name="requirements"></a><span data-ttu-id="16869-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16869-116">Requirements</span></span>



| <span data-ttu-id="16869-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16869-117">Requirement</span></span> | <span data-ttu-id="16869-118">Value</span><span class="sxs-lookup"><span data-stu-id="16869-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="16869-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16869-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16869-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="16869-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="16869-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16869-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16869-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="16869-122">None supported</span></span><br/>                                     |



 

 




