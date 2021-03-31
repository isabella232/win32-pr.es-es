---
title: Password (EapType), elemento
description: Obtenga información sobre el elemento Password (EapType). Este elemento identifica la contraseña del usuario o equipo que se autentica.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Elemento password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078386"
---
# <a name="password-eaptype-element"></a><span data-ttu-id="21dd0-105">Password (EapType), elemento</span><span class="sxs-lookup"><span data-stu-id="21dd0-105">Password (EapType) Element</span></span>

<span data-ttu-id="21dd0-106">El elemento **password (EapType)** identifica la contraseña del usuario o equipo que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="21dd0-106">The **Password (EapType)** element identifies the password of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="21dd0-107">El elemento de **contraseña** se define mediante el elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="21dd0-107">The **Password** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="21dd0-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21dd0-108">Remarks</span></span>

<span data-ttu-id="21dd0-109">Si el elemento **password (EapType)** no está presente, el hash de contraseña se obtiene de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="21dd0-109">If the **Password (EapType)** element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="21dd0-110">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="21dd0-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="21dd0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21dd0-111">Requirements</span></span>



| <span data-ttu-id="21dd0-112">Role</span><span class="sxs-lookup"><span data-stu-id="21dd0-112">Role</span></span> | <span data-ttu-id="21dd0-113">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="21dd0-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="21dd0-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="21dd0-114">Client</span></span><br/> | <span data-ttu-id="21dd0-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="21dd0-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="21dd0-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="21dd0-116">Server</span></span><br/> | <span data-ttu-id="21dd0-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="21dd0-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21dd0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="21dd0-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="21dd0-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="21dd0-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="21dd0-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="21dd0-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="21dd0-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="21dd0-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="21dd0-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="21dd0-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="21dd0-123">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="21dd0-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="21dd0-124">Esquema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="21dd0-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





