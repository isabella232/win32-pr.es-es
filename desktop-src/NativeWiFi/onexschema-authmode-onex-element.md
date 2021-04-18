---
description: Especifica el tipo de credenciales utilizado para la autenticación.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Elemento authMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687432"
---
# <a name="authmode-onex-element"></a><span data-ttu-id="e2366-103">Elemento authMode (OneX)</span><span class="sxs-lookup"><span data-stu-id="e2366-103">authMode (OneX) Element</span></span>

<span data-ttu-id="e2366-104">El elemento authMode (OneX) especifica el tipo de credenciales que se usan para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e2366-104">The authMode (OneX) element specifies the type of credentials used for authentication.</span></span> <span data-ttu-id="e2366-105">La siguiente tabla describe los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="e2366-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="e2366-106">Value</span><span class="sxs-lookup"><span data-stu-id="e2366-106">Value</span></span>         | <span data-ttu-id="e2366-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2366-107">Description</span></span>                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2366-108">machineOrUser</span><span class="sxs-lookup"><span data-stu-id="e2366-108">machineOrUser</span></span> | <span data-ttu-id="e2366-109">Usar credenciales de equipo o de usuario.</span><span class="sxs-lookup"><span data-stu-id="e2366-109">Use machine or user credentials.</span></span> <span data-ttu-id="e2366-110">Cuando un usuario ha iniciado sesión, se usan las credenciales del usuario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e2366-110">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="e2366-111">Cuando ningún usuario ha iniciado sesión, se usan las credenciales del equipo.</span><span class="sxs-lookup"><span data-stu-id="e2366-111">When no user is logged on, machine credentials are used.</span></span> |
| <span data-ttu-id="e2366-112">equipo</span><span class="sxs-lookup"><span data-stu-id="e2366-112">machine</span></span>       | <span data-ttu-id="e2366-113">Usar solo credenciales de equipo.</span><span class="sxs-lookup"><span data-stu-id="e2366-113">Use machine credentials only.</span></span>                                                                                                                                           |
| <span data-ttu-id="e2366-114">usuario</span><span class="sxs-lookup"><span data-stu-id="e2366-114">user</span></span>          | <span data-ttu-id="e2366-115">Usar solo credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="e2366-115">Use user credentials only.</span></span>                                                                                                                                              |
| <span data-ttu-id="e2366-116">guest</span><span class="sxs-lookup"><span data-stu-id="e2366-116">guest</span></span>         | <span data-ttu-id="e2366-117">Usar solo credenciales de invitado (vacío).</span><span class="sxs-lookup"><span data-stu-id="e2366-117">Use guest (empty) credentials only.</span></span>                                                                                                                                     |



 

<span data-ttu-id="e2366-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="e2366-118">This element is optional.</span></span> <span data-ttu-id="e2366-119">Cuando authMode no se especifica en un perfil, se usa un valor de `machineOrUser` .</span><span class="sxs-lookup"><span data-stu-id="e2366-119">When authMode is not specified in a profile, a value of `machineOrUser` is used.</span></span>

<span data-ttu-id="e2366-120">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="e2366-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="e2366-121">El elemento **authMode** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e2366-121">The **authMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2366-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2366-122">Remarks</span></span>

<span data-ttu-id="e2366-123">Este parámetro se puede establecer en la línea de comandos mediante el comando **netsh wlan set ProfileParameter**</span><span class="sxs-lookup"><span data-stu-id="e2366-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="e2366-124">Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="e2366-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2366-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2366-125">Requirements</span></span>



| <span data-ttu-id="e2366-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2366-126">Requirement</span></span> | <span data-ttu-id="e2366-127">Value</span><span class="sxs-lookup"><span data-stu-id="e2366-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2366-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2366-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2366-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e2366-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2366-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2366-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2366-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2366-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2366-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2366-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2366-133">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="e2366-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e2366-134">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="e2366-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="e2366-135">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="e2366-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e2366-136">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="e2366-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
