---
description: La \_ enumeración de tipo KEYSVC define si una clave se aplica a un equipo o a un servicio.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: Enumeración KEYSVC_TYPE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003118"
---
# <a name="keysvc_type-enumeration"></a><span data-ttu-id="75fbe-103">\_Enumeración de tipo KEYSVC</span><span class="sxs-lookup"><span data-stu-id="75fbe-103">KEYSVC\_TYPE enumeration</span></span>

<span data-ttu-id="75fbe-104">La enumeración de **\_ tipo KEYSVC** define si una clave se aplica a un equipo o a un servicio.</span><span class="sxs-lookup"><span data-stu-id="75fbe-104">The **KEYSVC\_TYPE** enumeration defines whether a key applies to a computer or a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="75fbe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75fbe-105">Syntax</span></span>


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a><span data-ttu-id="75fbe-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="75fbe-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="75fbe-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span><span class="sxs-lookup"><span data-stu-id="75fbe-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span></span>
</dt> <dd>

<span data-ttu-id="75fbe-108">La clave es para un equipo.</span><span class="sxs-lookup"><span data-stu-id="75fbe-108">The key is for a computer.</span></span>

</dd> <dt>

<span data-ttu-id="75fbe-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span><span class="sxs-lookup"><span data-stu-id="75fbe-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span></span>
</dt> <dd>

<span data-ttu-id="75fbe-110">La clave es para un servicio.</span><span class="sxs-lookup"><span data-stu-id="75fbe-110">The key is for a service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75fbe-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75fbe-111">Requirements</span></span>



| <span data-ttu-id="75fbe-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="75fbe-112">Requirement</span></span> | <span data-ttu-id="75fbe-113">Value</span><span class="sxs-lookup"><span data-stu-id="75fbe-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75fbe-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75fbe-114">Minimum supported client</span></span><br/> | <span data-ttu-id="75fbe-115">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="75fbe-115">None supported</span></span><br/>                                                             |
| <span data-ttu-id="75fbe-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75fbe-116">Minimum supported server</span></span><br/> | <span data-ttu-id="75fbe-117">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="75fbe-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75fbe-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75fbe-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="75fbe-119"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="75fbe-119"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75fbe-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="75fbe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75fbe-121">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="75fbe-121">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




