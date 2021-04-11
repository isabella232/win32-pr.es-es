---
description: Contiene información sobre el creador del perfil.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Elemento ProfileCreationType (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154472"
---
# <a name="profilecreationtype-mbnprofile-element"></a><span data-ttu-id="97154-103">Elemento ProfileCreationType (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="97154-103">ProfileCreationType (MBNProfile) Element</span></span>

<span data-ttu-id="97154-104">El elemento **ProfileCreationType (MBNProfile)** contiene información sobre el creador del perfil.</span><span class="sxs-lookup"><span data-stu-id="97154-104">The **ProfileCreationType (MBNProfile)** element contains information about the creator of the profile.</span></span>

<span data-ttu-id="97154-105">Este elemento puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="97154-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="97154-106">Value</span><span class="sxs-lookup"><span data-stu-id="97154-106">Value</span></span>                 | <span data-ttu-id="97154-107">Significado</span><span class="sxs-lookup"><span data-stu-id="97154-107">Meaning</span></span>                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97154-108">"UserProvisioned"</span><span class="sxs-lookup"><span data-stu-id="97154-108">"UserProvisioned"</span></span>     | <span data-ttu-id="97154-109">Este perfil se crea con la información proporcionada por el usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97154-109">This profile is created by information provided by the user of device.</span></span>                                                     |
| <span data-ttu-id="97154-110">"AdminProvisioned"</span><span class="sxs-lookup"><span data-stu-id="97154-110">"AdminProvisioned"</span></span>    | <span data-ttu-id="97154-111">Este perfil lo crean los administradores de ti y se distribuyen a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="97154-111">This profile is created by IT administrators and distributed to users.</span></span>                                                     |
| <span data-ttu-id="97154-112">"OperatorProvisioned"</span><span class="sxs-lookup"><span data-stu-id="97154-112">"OperatorProvisioned"</span></span> | <span data-ttu-id="97154-113">Este perfil lo crea un operador de red y se distribuye a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="97154-113">This profile is created by a network operator and distributed to users.</span></span>                                                    |
| <span data-ttu-id="97154-114">"DeviceProvisioned"</span><span class="sxs-lookup"><span data-stu-id="97154-114">"DeviceProvisioned"</span></span>   | <span data-ttu-id="97154-115">El servicio de banda ancha móvil crea este perfil mediante la información almacenada en el contexto aprovisionado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97154-115">This profile is created by the Mobile Broadband service by using the information stored in the device provisioned context.</span></span> |



 

<span data-ttu-id="97154-116">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="97154-116">This is an optional element.</span></span>

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="97154-117">El elemento **ProfileCreationType** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="97154-117">The **ProfileCreationType** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="97154-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97154-118">Requirements</span></span>



| <span data-ttu-id="97154-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="97154-119">Requirement</span></span> | <span data-ttu-id="97154-120">Value</span><span class="sxs-lookup"><span data-stu-id="97154-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="97154-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97154-121">Minimum supported client</span></span><br/> | <span data-ttu-id="97154-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="97154-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="97154-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97154-123">Minimum supported server</span></span><br/> | <span data-ttu-id="97154-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="97154-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="97154-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="97154-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="97154-126">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="97154-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="97154-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="97154-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="97154-128">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="97154-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="97154-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="97154-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




