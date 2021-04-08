---
description: Especifica si las credenciales del usuario se almacenan en caché para las conexiones posteriores.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Elemento cacheUserData (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001866"
---
# <a name="cacheuserdata-onex-element"></a><span data-ttu-id="66b4a-103">Elemento cacheUserData (OneX)</span><span class="sxs-lookup"><span data-stu-id="66b4a-103">cacheUserData (OneX) Element</span></span>

<span data-ttu-id="66b4a-104">El elemento cacheUserData (OneX) especifica si las credenciales del usuario se almacenan en caché para las conexiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="66b4a-104">The cacheUserData (OneX) element specifies whether the user credentials are cached for subsequent connections.</span></span> <span data-ttu-id="66b4a-105">Cuando cacheUserData es TRUE, las credenciales se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="66b4a-105">When cacheUserData is TRUE, the credentials are cached.</span></span> <span data-ttu-id="66b4a-106">Cuando cacheUserData es FALSE, las credenciales no se almacenan en caché y se puede solicitar credenciales al usuario en los intentos de conexión posteriores.</span><span class="sxs-lookup"><span data-stu-id="66b4a-106">When cacheUserData is FALSE, the credentials are not cached and the user may be prompted for credentials on subsequent connection attempts.</span></span>

<span data-ttu-id="66b4a-107">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="66b4a-107">This element is optional.</span></span> <span data-ttu-id="66b4a-108">Cuando cacheUserData no se especifica en un perfil, las credenciales de usuario se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="66b4a-108">When cacheUserData is not specified in a profile, the user credentials are cached.</span></span>

<span data-ttu-id="66b4a-109">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="66b4a-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

<span data-ttu-id="66b4a-110">El elemento **cacheUserData** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66b4a-110">The **cacheUserData** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b4a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66b4a-111">Requirements</span></span>



| <span data-ttu-id="66b4a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b4a-112">Requirement</span></span> | <span data-ttu-id="66b4a-113">Value</span><span class="sxs-lookup"><span data-stu-id="66b4a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="66b4a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66b4a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="66b4a-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="66b4a-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="66b4a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66b4a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="66b4a-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="66b4a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66b4a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="66b4a-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="66b4a-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="66b4a-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="66b4a-120">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="66b4a-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="66b4a-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="66b4a-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="66b4a-122">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="66b4a-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




