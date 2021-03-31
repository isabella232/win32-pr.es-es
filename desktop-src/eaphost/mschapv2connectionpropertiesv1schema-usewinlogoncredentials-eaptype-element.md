---
title: Elemento UseWinLogonCredentials (EapType)
description: Obtenga información sobre el elemento UseWinLogonCredentials (EapType). Este elemento controla el uso de las credenciales de WinLogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Elemento UseWinLogonCredentials EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793929"
---
# <a name="usewinlogoncredentials-eaptype-element"></a><span data-ttu-id="54f02-105">Elemento UseWinLogonCredentials (EapType)</span><span class="sxs-lookup"><span data-stu-id="54f02-105">UseWinLogonCredentials (EapType) Element</span></span>

<span data-ttu-id="54f02-106">El elemento **UseWinLogonCredentials (EapType)** controla el uso de las credenciales de WinLogin.</span><span class="sxs-lookup"><span data-stu-id="54f02-106">The **UseWinLogonCredentials (EapType)** element controls use of the winlogin credentials.</span></span>

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

<span data-ttu-id="54f02-107">El elemento **UseWinLogonCredentials** se define mediante el elemento [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="54f02-107">The **UseWinLogonCredentials** element is defined by the [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="54f02-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54f02-108">Remarks</span></span>

<span data-ttu-id="54f02-109">Si es TRUE, EAP MS-CHAPv2 obtiene las credenciales de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="54f02-109">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="54f02-110">Si es FALSE, EAP MS-CHAPv2 obtiene las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="54f02-110">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <span data-ttu-id="54f02-111">El elemento **UseWinLogonCredentials (EapType)** es opcional.</span><span class="sxs-lookup"><span data-stu-id="54f02-111">The **UseWinLogonCredentials (EapType)** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="54f02-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54f02-112">Requirements</span></span>



| <span data-ttu-id="54f02-113">Role</span><span class="sxs-lookup"><span data-stu-id="54f02-113">Role</span></span> | <span data-ttu-id="54f02-114">Versiones mínimas admitidas del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="54f02-114">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="54f02-115">Remoto</span><span class="sxs-lookup"><span data-stu-id="54f02-115">Client</span></span><br/> | <span data-ttu-id="54f02-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="54f02-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="54f02-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="54f02-117">Server</span></span><br/> | <span data-ttu-id="54f02-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="54f02-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54f02-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="54f02-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="54f02-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="54f02-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="54f02-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="54f02-121">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="54f02-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="54f02-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="54f02-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="54f02-123">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="54f02-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="54f02-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="54f02-125">Esquema mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="54f02-125">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





