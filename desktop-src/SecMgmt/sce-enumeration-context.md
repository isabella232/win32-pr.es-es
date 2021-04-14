---
description: El \_ tipo de datos de contexto de enumeración de SCE \_ es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. La función información de consulta PFSCE la usa \_ \_ para navegar por la base de datos de seguridad.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360222"
---
# <a name="sce_enumeration_context"></a><span data-ttu-id="285f9-104">\_contexto de enumeración de SCE \_</span><span class="sxs-lookup"><span data-stu-id="285f9-104">SCE\_ENUMERATION\_CONTEXT</span></span>

<span data-ttu-id="285f9-105">El tipo de datos de **\_ \_ contexto de enumeración de SCE** es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="285f9-105">The **SCE\_ENUMERATION\_CONTEXT** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="285f9-106">La función [**\_ \_ información de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) la usa para navegar por la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="285f9-106">It is used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a><span data-ttu-id="285f9-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="285f9-107">Requirements</span></span>



| <span data-ttu-id="285f9-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="285f9-108">Requirement</span></span> | <span data-ttu-id="285f9-109">Value</span><span class="sxs-lookup"><span data-stu-id="285f9-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="285f9-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="285f9-110">Minimum supported client</span></span><br/> | <span data-ttu-id="285f9-111">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="285f9-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="285f9-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="285f9-112">Minimum supported server</span></span><br/> | <span data-ttu-id="285f9-113">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="285f9-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="285f9-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="285f9-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="285f9-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="285f9-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="285f9-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="285f9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285f9-117">**\_información de consulta de PFSCE \_**</span><span class="sxs-lookup"><span data-stu-id="285f9-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

