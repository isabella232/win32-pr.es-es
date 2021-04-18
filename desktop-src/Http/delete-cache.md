---
title: delete cache
description: Vacía la memoria caché de la dirección URL completa o elimina las entradas según la dirección URL especificada.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- eliminar caché HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "105685666"
---
# <a name="delete-cache"></a><span data-ttu-id="b08ca-104">delete cache</span><span class="sxs-lookup"><span data-stu-id="b08ca-104">delete cache</span></span>

<span data-ttu-id="b08ca-105">Vacía la memoria caché de la dirección URL completa o elimina las entradas según la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="b08ca-105">Flushes the entire URL cache or deletes entries according to the specified URL.</span></span>

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="b08ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b08ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b08ca-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* cadena*</span><span class="sxs-lookup"><span data-stu-id="b08ca-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="b08ca-108">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b08ca-108">Required.</span></span> <span data-ttu-id="b08ca-109">Especifica la dirección URL completa.</span><span class="sxs-lookup"><span data-stu-id="b08ca-109">Specifies the fully qualified URL.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b08ca-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[Recursive = \] {sí \| no}**</span><span class="sxs-lookup"><span data-stu-id="b08ca-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive=\]{yes\|no}**</span></span>
</dt> <dd>

<span data-ttu-id="b08ca-111">En caso afirmativo, quita todas las entradas de la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="b08ca-111">If yes, removes all entries under the specified URL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b08ca-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b08ca-112">Examples</span></span>

<span data-ttu-id="b08ca-113">**eliminar la dirección URL de caché = https://www.contoso.com:80/myresource/ recursivo = sí**</span><span class="sxs-lookup"><span data-stu-id="b08ca-113">**delete cache url=https://www.contoso.com:80/myresource/ recursive=yes**</span></span>

 

 




