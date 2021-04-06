---
description: Especifica la configuración de conexión automática que se va a usar para un dispositivo de banda ancha móvil.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: Elemento ConnectionMode (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001123"
---
# <a name="connectionmode-mbnprofile-element"></a><span data-ttu-id="520b2-103">Elemento ConnectionMode (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="520b2-103">ConnectionMode (MBNProfile) Element</span></span>

<span data-ttu-id="520b2-104">El elemento **ConnectionMode (MBNProfile)** especifica la configuración de conexión automática que se va a usar para un dispositivo de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="520b2-104">The **ConnectionMode (MBNProfile)** element specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="520b2-105">Este elemento puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="520b2-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="520b2-106">Value</span><span class="sxs-lookup"><span data-stu-id="520b2-106">Value</span></span>       | <span data-ttu-id="520b2-107">Significado</span><span class="sxs-lookup"><span data-stu-id="520b2-107">Meaning</span></span>                                                                |
|-------------|------------------------------------------------------------------------|
| <span data-ttu-id="520b2-108">manualmente</span><span class="sxs-lookup"><span data-stu-id="520b2-108">"manual"</span></span>    | <span data-ttu-id="520b2-109">Nunca se conecta automáticamente a la red.</span><span class="sxs-lookup"><span data-stu-id="520b2-109">Never automatically connect to the network.</span></span>                            |
| <span data-ttu-id="520b2-110">automática</span><span class="sxs-lookup"><span data-stu-id="520b2-110">"auto"</span></span>      | <span data-ttu-id="520b2-111">Conéctese siempre automáticamente a la red.</span><span class="sxs-lookup"><span data-stu-id="520b2-111">Always automatically connect to the network.</span></span>                           |
| <span data-ttu-id="520b2-112">"auto-Home"</span><span class="sxs-lookup"><span data-stu-id="520b2-112">"auto-home"</span></span> | <span data-ttu-id="520b2-113">Conectarse automáticamente a la red excepto cuando se encuentre en una red móvil.</span><span class="sxs-lookup"><span data-stu-id="520b2-113">Automatically connect to the network except when in a roaming network.</span></span> |



 

<span data-ttu-id="520b2-114">Este elemento puede tener un máximo de una repetición.</span><span class="sxs-lookup"><span data-stu-id="520b2-114">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="520b2-115">Esto es un elemento requerido.</span><span class="sxs-lookup"><span data-stu-id="520b2-115">This is a required element.</span></span>

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="520b2-116">El elemento **ConnectionMode** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="520b2-116">The **ConnectionMode** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="520b2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="520b2-117">Requirements</span></span>



| <span data-ttu-id="520b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="520b2-118">Requirement</span></span> | <span data-ttu-id="520b2-119">Value</span><span class="sxs-lookup"><span data-stu-id="520b2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="520b2-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="520b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="520b2-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="520b2-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="520b2-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="520b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="520b2-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="520b2-123">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="520b2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="520b2-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="520b2-125">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="520b2-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="520b2-126">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="520b2-126">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="520b2-127">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="520b2-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="520b2-128">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="520b2-128">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




