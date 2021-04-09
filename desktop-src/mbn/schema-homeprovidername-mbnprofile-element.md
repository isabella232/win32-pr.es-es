---
description: Identifica el nombre del proveedor de inicio de la SIM o el dispositivo especificados.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Elemento HomeProviderName (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809619"
---
# <a name="homeprovidername-mbnprofile-element"></a><span data-ttu-id="694a9-103">Elemento HomeProviderName (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="694a9-103">HomeProviderName (MBNProfile) Element</span></span>

<span data-ttu-id="694a9-104">El elemento **HomeProviderName (MBNProfile)** identifica el nombre del proveedor de inicio de la SIM o el dispositivo especificados.</span><span class="sxs-lookup"><span data-stu-id="694a9-104">The **HomeProviderName (MBNProfile)** element identifies the name of Home provider for the given SIM/Device.</span></span>

<span data-ttu-id="694a9-105">Este elemento es opcional y lo establece el servicio de banda ancha móvil para uso interno.</span><span class="sxs-lookup"><span data-stu-id="694a9-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="694a9-106">Una aplicación no debe establecer este campo al crear o actualizar un perfil.</span><span class="sxs-lookup"><span data-stu-id="694a9-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="694a9-107">El elemento **HomeProviderName** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="694a9-107">The **HomeProviderName** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="694a9-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="694a9-108">Requirements</span></span>



| <span data-ttu-id="694a9-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="694a9-109">Requirement</span></span> | <span data-ttu-id="694a9-110">Value</span><span class="sxs-lookup"><span data-stu-id="694a9-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="694a9-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="694a9-111">Minimum supported client</span></span><br/> | <span data-ttu-id="694a9-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="694a9-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="694a9-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="694a9-113">Minimum supported server</span></span><br/> | <span data-ttu-id="694a9-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="694a9-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="694a9-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="694a9-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="694a9-116">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="694a9-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="694a9-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="694a9-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="694a9-118">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="694a9-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="694a9-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="694a9-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




