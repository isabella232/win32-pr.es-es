---
description: Un tipo de datos opaco.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277013"
---
# <a name="plsa_client_request"></a><span data-ttu-id="39202-103">\_solicitud de cliente PLSA \_</span><span class="sxs-lookup"><span data-stu-id="39202-103">PLSA\_CLIENT\_REQUEST</span></span>

<span data-ttu-id="39202-104">El tipo de datos de la **\_ \_ solicitud de cliente PLSA** es un tipo de datos opaco.</span><span class="sxs-lookup"><span data-stu-id="39202-104">The **PLSA\_CLIENT\_REQUEST** data type is an opaque data type.</span></span>

<span data-ttu-id="39202-105">La [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) la usa internamente para mantener la información de cliente relacionada con las solicitudes individuales.</span><span class="sxs-lookup"><span data-stu-id="39202-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) uses it internally to maintain client information related to individual requests.</span></span>


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a><span data-ttu-id="39202-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39202-106">Requirements</span></span>



| <span data-ttu-id="39202-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="39202-107">Requirement</span></span> | <span data-ttu-id="39202-108">Value</span><span class="sxs-lookup"><span data-stu-id="39202-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39202-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39202-109">Minimum supported client</span></span><br/> | <span data-ttu-id="39202-110">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="39202-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="39202-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39202-111">Minimum supported server</span></span><br/> | <span data-ttu-id="39202-112">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="39202-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39202-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39202-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="39202-114"><dt>Ntsecpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="39202-114"><dt>Ntsecpkg.h</dt></span></span> </dl> |



 

 
