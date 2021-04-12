---
title: show cachestate
description: Enumera todos los recursos y sus propiedades asociadas que se almacenan en caché en la caché de respuesta HTTP o muestra un único recurso y sus propiedades asociadas.
ms.assetid: 9daa445e-dd2f-4b73-8938-58df931c015b
keywords:
- Mostrar cachestate HTTP
topic_type:
- apiref
api_name:
- show cachestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088a59eaa92db8ed9e8cbe59075d540507e51535
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104358365"
---
# <a name="show-cachestate"></a><span data-ttu-id="d887f-104">show cachestate</span><span class="sxs-lookup"><span data-stu-id="d887f-104">show cachestate</span></span>

<span data-ttu-id="d887f-105">Enumera todos los recursos y sus propiedades asociadas que se almacenan en caché en la caché de respuesta HTTP o muestra un único recurso y sus propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d887f-105">Lists all resources and their associated properties that are cached in the HTTP response cache or displays a single resource and its associated properties.</span></span>

``` syntax
show cachestate [[url=]string]
 
```

## <a name="parameters"></a><span data-ttu-id="d887f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d887f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d887f-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[URL = \] ***cadena***\]**</span><span class="sxs-lookup"><span data-stu-id="d887f-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[url=\]***string***\]**</span></span>
</dt> <dd>

<span data-ttu-id="d887f-108">Dirección URL completa.</span><span class="sxs-lookup"><span data-stu-id="d887f-108">Fully qualified URL.</span></span> <span data-ttu-id="d887f-109">Si no se especifica, implica todas las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="d887f-109">If unspecified, implies all URLs.</span></span> <span data-ttu-id="d887f-110">La dirección URL también puede ser un prefijo para las direcciones URL registradas.</span><span class="sxs-lookup"><span data-stu-id="d887f-110">The URL can also be a prefix to registered URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d887f-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d887f-111">Examples</span></span>

<span data-ttu-id="d887f-112">**Mostrar dirección URL de cachestate =https://www.contoso.com:80/myresource**</span><span class="sxs-lookup"><span data-stu-id="d887f-112">**show cachestate url=https://www.contoso.com:80/myresource**</span></span>

 

 




