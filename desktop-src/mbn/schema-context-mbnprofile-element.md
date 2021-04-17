---
description: Especifica los parámetros necesarios para configurar una conexión de datos.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Elemento context (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696558"
---
# <a name="context-mbnprofile-element"></a><span data-ttu-id="b9eb3-103">Elemento context (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="b9eb3-103">Context (MBNProfile) Element</span></span>

<span data-ttu-id="b9eb3-104">El elemento **context (MBNProfile)** especifica los parámetros necesarios para configurar una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-104">The **Context (MBNProfile)** element specifies the parameters required to setup a data connection.</span></span>

<span data-ttu-id="b9eb3-105">El elemento puede tener los siguientes elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-105">The element can have the following child elements.</span></span>

-   [<span data-ttu-id="b9eb3-106">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="b9eb3-106">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)
-   [<span data-ttu-id="b9eb3-107">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="b9eb3-107">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
-   [<span data-ttu-id="b9eb3-108">**Compresión**</span><span class="sxs-lookup"><span data-stu-id="b9eb3-108">**Compression**</span></span>](schema-compression-contexttype-element.md)
-   [<span data-ttu-id="b9eb3-109">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="b9eb3-109">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)

<span data-ttu-id="b9eb3-110">Este elemento puede tener un máximo de una repetición.</span><span class="sxs-lookup"><span data-stu-id="b9eb3-110">This element can have a maximum of one occurrence.</span></span>

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

<span data-ttu-id="b9eb3-111">El elemento de **contexto** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b9eb3-111">The **Context** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9eb3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9eb3-112">Requirements</span></span>



| <span data-ttu-id="b9eb3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9eb3-113">Requirement</span></span> | <span data-ttu-id="b9eb3-114">Value</span><span class="sxs-lookup"><span data-stu-id="b9eb3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="b9eb3-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9eb3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b9eb3-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="b9eb3-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="b9eb3-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9eb3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b9eb3-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b9eb3-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="b9eb3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9eb3-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9eb3-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="b9eb3-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b9eb3-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="b9eb3-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="b9eb3-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="b9eb3-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b9eb3-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="b9eb3-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




