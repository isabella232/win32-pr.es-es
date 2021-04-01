---
description: Especifica, en segundos, el retraso máximo antes de que se produzca un error en el intento de conexión de inicio de sesión único.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Elemento maxDelay (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909430"
---
# <a name="maxdelay-singlesignon-element"></a><span data-ttu-id="ed6f2-103">Elemento maxDelay (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="ed6f2-103">maxDelay (singleSignOn) Element</span></span>

<span data-ttu-id="ed6f2-104">El elemento maxDelay (singleSignOn) especifica, en segundos, el retraso máximo antes de que se produzca un error en el intento de conexión de inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="ed6f2-104">The maxDelay (singleSignOn) element specifies, in seconds, the maximum delay before the single sign on connection attempt fails.</span></span>

<span data-ttu-id="ed6f2-105">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="ed6f2-105">This element is optional.</span></span> <span data-ttu-id="ed6f2-106">Cuando maxDelay no se especifica en un perfil, se usa un valor de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="ed6f2-106">When maxDelay is not specified in a profile, a value of 10 seconds is used.</span></span>

<span data-ttu-id="ed6f2-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="ed6f2-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ed6f2-108">El elemento **maxDelay** se define mediante el elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ed6f2-108">The **maxDelay** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed6f2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed6f2-109">Remarks</span></span>

<span data-ttu-id="ed6f2-110">Este parámetro se puede establecer en la línea de comandos mediante el comando **netsh wlan set ProfileParameter**</span><span class="sxs-lookup"><span data-stu-id="ed6f2-110">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="ed6f2-111">Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="ed6f2-111">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed6f2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed6f2-112">Requirements</span></span>



| <span data-ttu-id="ed6f2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed6f2-113">Requirement</span></span> | <span data-ttu-id="ed6f2-114">Value</span><span class="sxs-lookup"><span data-stu-id="ed6f2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ed6f2-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed6f2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ed6f2-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ed6f2-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ed6f2-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed6f2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ed6f2-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed6f2-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed6f2-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed6f2-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed6f2-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="ed6f2-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ed6f2-121">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="ed6f2-121">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="ed6f2-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="ed6f2-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ed6f2-123">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ed6f2-123">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
