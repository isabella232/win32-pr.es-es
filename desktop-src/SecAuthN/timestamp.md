---
description: El tipo de datos TimeStamp contiene información sobre la validez temporal de los tokens de seguridad. El formato del valor del tipo de datos TimeStamp es el mismo que el de la estructura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Marca de tiempo (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648297"
---
# <a name="timestamp"></a><span data-ttu-id="effa0-104">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="effa0-104">TimeStamp</span></span>

<span data-ttu-id="effa0-105">El tipo de datos **timestamp** contiene información sobre la validez temporal de los tokens de seguridad.</span><span class="sxs-lookup"><span data-stu-id="effa0-105">The **TimeStamp** data type holds information about the time validity of security tokens.</span></span> <span data-ttu-id="effa0-106">El formato del valor del tipo de datos **timestamp** es el mismo que el de la estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="effa0-106">The format of the value of the **TimeStamp** data type is the same as that of the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a><span data-ttu-id="effa0-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="effa0-107">Requirements</span></span>



| <span data-ttu-id="effa0-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="effa0-108">Requirement</span></span> | <span data-ttu-id="effa0-109">Value</span><span class="sxs-lookup"><span data-stu-id="effa0-109">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effa0-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="effa0-110">Minimum supported client</span></span><br/> | <span data-ttu-id="effa0-111">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="effa0-111">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="effa0-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="effa0-112">Minimum supported server</span></span><br/> | <span data-ttu-id="effa0-113">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="effa0-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="effa0-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="effa0-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="effa0-115"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="effa0-115"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |



 

 
