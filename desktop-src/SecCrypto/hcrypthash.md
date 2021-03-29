---
description: El tipo de datos HCRYPTHASH se usa para representar los identificadores de los objetos hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912030"
---
# <a name="hcrypthash"></a><span data-ttu-id="009d8-103">HCRYPTHASH</span><span class="sxs-lookup"><span data-stu-id="009d8-103">HCRYPTHASH</span></span>

<span data-ttu-id="009d8-104">El tipo de datos **HCRYPTHASH** se usa para representar los identificadores de los [*objetos hash*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="009d8-104">The **HCRYPTHASH** data type is used to represent handles to [*hash objects*](../secgloss/h-gly.md).</span></span> <span data-ttu-id="009d8-105">Estos identificadores indican al módulo CSP qué hash se usa en una operación determinada.</span><span class="sxs-lookup"><span data-stu-id="009d8-105">These handles indicate to the CSP module which hash is being used in a particular operation.</span></span> <span data-ttu-id="009d8-106">El módulo CSP no habilita la manipulación directa de los valores hash.</span><span class="sxs-lookup"><span data-stu-id="009d8-106">The CSP module does not enable direct manipulation of the hash values.</span></span> <span data-ttu-id="009d8-107">En su lugar, el usuario manipula los valores hash a través del identificador hash.</span><span class="sxs-lookup"><span data-stu-id="009d8-107">Instead, the user manipulates the hash values through the hash handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a><span data-ttu-id="009d8-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="009d8-108">Requirements</span></span>



| <span data-ttu-id="009d8-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="009d8-109">Requirement</span></span> | <span data-ttu-id="009d8-110">Value</span><span class="sxs-lookup"><span data-stu-id="009d8-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="009d8-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="009d8-111">Minimum supported client</span></span><br/> | <span data-ttu-id="009d8-112">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="009d8-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="009d8-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="009d8-113">Minimum supported server</span></span><br/> | <span data-ttu-id="009d8-114">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="009d8-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="009d8-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="009d8-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="009d8-116"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="009d8-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
