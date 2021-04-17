---
description: Especifica el número máximo de mensajes de EAPOL-Start enviados.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Elemento maxStart (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677750"
---
# <a name="maxstart-onex-element"></a><span data-ttu-id="0c65d-103">Elemento maxStart (OneX)</span><span class="sxs-lookup"><span data-stu-id="0c65d-103">maxStart (OneX) Element</span></span>

<span data-ttu-id="0c65d-104">El elemento maxStart (OneX) especifica el número máximo de mensajes EAPOL-Start enviados.</span><span class="sxs-lookup"><span data-stu-id="0c65d-104">The maxStart (OneX) element specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="0c65d-105">Una vez enviado el número máximo de mensajes EAPOL-Start, el cliente supone que no hay ningún autenticador presente en la red.</span><span class="sxs-lookup"><span data-stu-id="0c65d-105">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="0c65d-106">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="0c65d-106">This element is optional.</span></span> <span data-ttu-id="0c65d-107">Cuando maxStart no se especifica en un perfil, se usa un valor de 3 mensajes.</span><span class="sxs-lookup"><span data-stu-id="0c65d-107">When maxStart is not specified in a profile, a value of 3 messages is used.</span></span>

<span data-ttu-id="0c65d-108">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="0c65d-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="0c65d-109">El elemento **maxStart** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0c65d-109">The **maxStart** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c65d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c65d-110">Requirements</span></span>



| <span data-ttu-id="0c65d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c65d-111">Requirement</span></span> | <span data-ttu-id="0c65d-112">Value</span><span class="sxs-lookup"><span data-stu-id="0c65d-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c65d-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c65d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0c65d-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0c65d-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c65d-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c65d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0c65d-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c65d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c65d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c65d-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c65d-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="0c65d-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0c65d-119">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="0c65d-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="0c65d-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="0c65d-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0c65d-121">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="0c65d-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




