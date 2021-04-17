---
description: El tipo de datos de identificador de KEYSVCC \_ define un identificador de servicio de claves. \_Las funciones RKeyOpenKeyService y RKeyCloseKeyService usan un identificador de identificador de KEYSVCC.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1427a4ffd4637e073e517e5df54af72191992d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668329"
---
# <a name="keysvcc_handle"></a><span data-ttu-id="20774-104">identificador de KEYSVCC \_</span><span class="sxs-lookup"><span data-stu-id="20774-104">KEYSVCC\_HANDLE</span></span>

<span data-ttu-id="20774-105">El tipo de datos de **\_ identificador de KEYSVCC** define un identificador de servicio de claves.</span><span class="sxs-lookup"><span data-stu-id="20774-105">The **KEYSVCC\_HANDLE** data type defines a key service handle.</span></span> <span data-ttu-id="20774-106">Las funciones [**RKeyOpenKeyService**](rkeyopenkeyservice.md) y [**RKeyCloseKeyService**](rkeyclosekeyservice.md) usan un identificador de **\_ identificador de KEYSVCC** .</span><span class="sxs-lookup"><span data-stu-id="20774-106">A **KEYSVCC\_HANDLE** handle is used by the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) and [**RKeyCloseKeyService**](rkeyclosekeyservice.md) functions.</span></span>


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="20774-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20774-107">Requirements</span></span>



| <span data-ttu-id="20774-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="20774-108">Requirement</span></span> | <span data-ttu-id="20774-109">Value</span><span class="sxs-lookup"><span data-stu-id="20774-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20774-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20774-110">Minimum supported client</span></span><br/> | <span data-ttu-id="20774-111">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="20774-111">None supported</span></span><br/>                                                             |
| <span data-ttu-id="20774-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20774-112">Minimum supported server</span></span><br/> | <span data-ttu-id="20774-113">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="20774-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20774-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20774-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="20774-115"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="20774-115"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20774-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="20774-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20774-117">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="20774-117">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="20774-118">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="20774-118">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




