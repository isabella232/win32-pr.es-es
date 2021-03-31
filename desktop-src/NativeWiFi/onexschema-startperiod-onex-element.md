---
description: Especifica el período de tiempo, en segundos, que hay que esperar antes de que se envíe un EAPOL-Start.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: Elemento startPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360668"
---
# <a name="startperiod-onex-element"></a><span data-ttu-id="ced5c-103">Elemento startPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="ced5c-103">startPeriod (OneX) Element</span></span>

<span data-ttu-id="ced5c-104">El elemento startPeriod (OneX) especifica el período de tiempo, en segundos, que hay que esperar antes de que se envíe un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="ced5c-104">The startPeriod (OneX) element specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="ced5c-105">Se envía un mensaje de EAPOL-Start para iniciar el proceso de autenticación de 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="ced5c-105">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span>

<span data-ttu-id="ced5c-106">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="ced5c-106">This element is optional.</span></span> <span data-ttu-id="ced5c-107">Cuando startPeriod no se especifica en un perfil, se usa un valor de 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="ced5c-107">When startPeriod is not specified in a profile, a value of 5 seconds is used.</span></span>

<span data-ttu-id="ced5c-108">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="ced5c-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="startPeriod">
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

<span data-ttu-id="ced5c-109">El elemento **startPeriod** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ced5c-109">The **startPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ced5c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ced5c-110">Requirements</span></span>



| <span data-ttu-id="ced5c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ced5c-111">Requirement</span></span> | <span data-ttu-id="ced5c-112">Value</span><span class="sxs-lookup"><span data-stu-id="ced5c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ced5c-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ced5c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ced5c-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ced5c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ced5c-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ced5c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ced5c-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ced5c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ced5c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ced5c-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="ced5c-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="ced5c-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ced5c-119">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="ced5c-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="ced5c-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="ced5c-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ced5c-121">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="ced5c-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




