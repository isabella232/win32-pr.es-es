---
description: Especifica el período de tiempo máximo, en segundos, en el que un cliente espera una respuesta del autenticador.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Elemento authPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 098391a672eedd2657dbd7ad5913fef13fde98cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082620"
---
# <a name="authperiod-onex-element"></a><span data-ttu-id="9c6b1-103">Elemento authPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="9c6b1-103">authPeriod (OneX) Element</span></span>

<span data-ttu-id="9c6b1-104">El elemento authPeriod (OneX) especifica el período de tiempo máximo, en segundos, en el que un cliente espera una respuesta del autenticador.</span><span class="sxs-lookup"><span data-stu-id="9c6b1-104">The authPeriod (OneX) element specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="9c6b1-105">Si no se recibe una respuesta dentro del período especificado, el cliente da por supuesto que no hay ningún autenticador presente en la red.</span><span class="sxs-lookup"><span data-stu-id="9c6b1-105">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="9c6b1-106">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="9c6b1-106">This element is optional.</span></span> <span data-ttu-id="9c6b1-107">Cuando authPeriod no se especifica en un perfil, se usa un valor de 18 segundos.</span><span class="sxs-lookup"><span data-stu-id="9c6b1-107">When authPeriod is not specified in a profile, a value of 18 seconds is used.</span></span>

<span data-ttu-id="9c6b1-108">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="9c6b1-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="9c6b1-109">El elemento **authPeriod** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9c6b1-109">The **authPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c6b1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c6b1-110">Requirements</span></span>



| <span data-ttu-id="9c6b1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c6b1-111">Requirement</span></span> | <span data-ttu-id="9c6b1-112">Value</span><span class="sxs-lookup"><span data-stu-id="9c6b1-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c6b1-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c6b1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9c6b1-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c6b1-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c6b1-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c6b1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9c6b1-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c6b1-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c6b1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c6b1-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c6b1-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="9c6b1-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9c6b1-119">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="9c6b1-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="9c6b1-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="9c6b1-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9c6b1-121">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="9c6b1-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




