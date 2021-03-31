---
title: Username (elemento) (CHAP)
description: Obtenga información sobre el elemento username, que identifica al usuario que se está autenticando. Vea un ejemplo de sintaxis y vea más recursos disponibles.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Username (elemento) EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995629"
---
# <a name="username-element-chap"></a><span data-ttu-id="1ba01-105">Username (elemento) (CHAP)</span><span class="sxs-lookup"><span data-stu-id="1ba01-105">Username element (CHAP)</span></span>

<span data-ttu-id="1ba01-106">El elemento **username** identifica el usuario que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="1ba01-106">The **Username** element identifies the user being authenticated.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a><span data-ttu-id="1ba01-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ba01-107">Remarks</span></span>

<span data-ttu-id="1ba01-108">Si el elemento **username** no está presente, el nombre de usuario se obtiene de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="1ba01-108">If the **Username** element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="1ba01-109">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1ba01-109">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba01-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ba01-110">Requirements</span></span>



| <span data-ttu-id="1ba01-111">Role</span><span class="sxs-lookup"><span data-stu-id="1ba01-111">Role</span></span> | <span data-ttu-id="1ba01-112">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1ba01-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="1ba01-113">Remoto</span><span class="sxs-lookup"><span data-stu-id="1ba01-113">Client</span></span><br/> | <span data-ttu-id="1ba01-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ba01-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1ba01-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="1ba01-115">Server</span></span><br/> | <span data-ttu-id="1ba01-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ba01-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ba01-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ba01-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba01-118">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="1ba01-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1ba01-119">Esquema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1ba01-119">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





