---
description: El tipo de datos HCRYPTKEY se usa para representar los identificadores de las claves criptográficas.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668214"
---
# <a name="hcryptkey"></a><span data-ttu-id="d7fbd-103">HCRYPTKEY</span><span class="sxs-lookup"><span data-stu-id="d7fbd-103">HCRYPTKEY</span></span>

<span data-ttu-id="d7fbd-104">El tipo de datos **HCRYPTKEY** se usa para representar los identificadores de [*las claves criptográficas*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d7fbd-104">The **HCRYPTKEY** data type is used to represent handles to [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="d7fbd-105">Estos identificadores se usan para indicar al módulo CSP qué clave se usa en una operación específica.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-105">These handles are used to indicate to the CSP module which key is being used in a specific operation.</span></span> <span data-ttu-id="d7fbd-106">El módulo CSP no permite el acceso directo a los valores de clave.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-106">The CSP module does not enable direct access to the key values.</span></span> <span data-ttu-id="d7fbd-107">En su lugar, el usuario realiza funciones mediante el uso del valor de clave a través del identificador de clave.</span><span class="sxs-lookup"><span data-stu-id="d7fbd-107">Instead, the user performs functions by using the key value through the key handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a><span data-ttu-id="d7fbd-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7fbd-108">Requirements</span></span>



| <span data-ttu-id="d7fbd-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7fbd-109">Requirement</span></span> | <span data-ttu-id="d7fbd-110">Value</span><span class="sxs-lookup"><span data-stu-id="d7fbd-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fbd-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7fbd-111">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fbd-112">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d7fbd-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7fbd-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7fbd-113">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fbd-114">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7fbd-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7fbd-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7fbd-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7fbd-116"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7fbd-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
