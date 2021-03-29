---
title: show urlacl
description: Muestra las listas DACL de la dirección URL reservada especificada o de todas las direcciones URL reservadas.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- Mostrar urlacl HTTP
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86f7856e70a1be327297bb3fd4b892b3bf39789
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "103994783"
---
# <a name="show-urlacl"></a><span data-ttu-id="00ebf-104">show urlacl</span><span class="sxs-lookup"><span data-stu-id="00ebf-104">show urlacl</span></span>

<span data-ttu-id="00ebf-105">Muestra las listas DACL de la dirección URL reservada especificada o de todas las direcciones URL reservadas.</span><span class="sxs-lookup"><span data-stu-id="00ebf-105">Lists DACLs for the specified reserved URL or all reserved URLs.</span></span>

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a><span data-ttu-id="00ebf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00ebf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ebf-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* cadena*</span><span class="sxs-lookup"><span data-stu-id="00ebf-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="00ebf-108">Especifica la dirección URL completa.</span><span class="sxs-lookup"><span data-stu-id="00ebf-108">Specifies the fully qualified URL.</span></span> <span data-ttu-id="00ebf-109">Si no se especifica, implica todas las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="00ebf-109">If unspecified, implies all URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="00ebf-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="00ebf-110">Examples</span></span>

<span data-ttu-id="00ebf-111">**Mostrar dirección URL de urlacl =https://+:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="00ebf-111">**show urlacl url=https://+:80/MyUrl**</span></span>

<span data-ttu-id="00ebf-112">**Mostrar dirección URL de urlacl =https://www.contoso.com:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="00ebf-112">**show urlacl url=https://www.contoso.com:80/MyUrl**</span></span>

 

 




