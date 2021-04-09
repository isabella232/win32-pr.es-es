---
description: El tipo de datos de identificador de SCE \_ es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. Lo usan \_ las funciones PFSCE Query \_ info y PFSCE \_ set \_ info support para pasar información entre los datos adjuntos y la base de datos de seguridad.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154074"
---
# <a name="sce_handle"></a><span data-ttu-id="6959f-104">identificador de SCE \_</span><span class="sxs-lookup"><span data-stu-id="6959f-104">SCE\_HANDLE</span></span>

<span data-ttu-id="6959f-105">El tipo de datos de **\_ identificador de SCE** es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6959f-105">The **SCE\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="6959f-106">Lo usan las funciones [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support para pasar información entre los datos adjuntos y la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6959f-106">It is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support functions to pass information between the attachment and the security database.</span></span>


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="6959f-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6959f-107">Requirements</span></span>



| <span data-ttu-id="6959f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="6959f-108">Requirement</span></span> | <span data-ttu-id="6959f-109">Value</span><span class="sxs-lookup"><span data-stu-id="6959f-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6959f-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6959f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6959f-111">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6959f-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6959f-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6959f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6959f-113">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6959f-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6959f-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6959f-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="6959f-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="6959f-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6959f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="6959f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6959f-117">**\_información de consulta de PFSCE \_**</span><span class="sxs-lookup"><span data-stu-id="6959f-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[<span data-ttu-id="6959f-118">**PFSCE \_ establecer \_ información**</span><span class="sxs-lookup"><span data-stu-id="6959f-118">**PFSCE\_SET\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

