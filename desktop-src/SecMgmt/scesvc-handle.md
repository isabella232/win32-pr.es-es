---
description: El tipo de datos de identificador de SCESVC \_ es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540974"
---
# <a name="scesvc_handle"></a><span data-ttu-id="3b975-103">identificador de SCESVC \_</span><span class="sxs-lookup"><span data-stu-id="3b975-103">SCESVC\_HANDLE</span></span>

<span data-ttu-id="3b975-104">El tipo de datos de **\_ identificador de SCESVC** es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3b975-104">The **SCESVC\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="3b975-105">Lo usan los métodos de las interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) y [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para pasar información entre el complemento configuración de seguridad y la extensión del complemento.</span><span class="sxs-lookup"><span data-stu-id="3b975-105">It is used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span>


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="3b975-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b975-106">Requirements</span></span>



| <span data-ttu-id="3b975-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b975-107">Requirement</span></span> | <span data-ttu-id="3b975-108">Value</span><span class="sxs-lookup"><span data-stu-id="3b975-108">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b975-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b975-109">Minimum supported client</span></span><br/> | <span data-ttu-id="3b975-110">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3b975-110">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3b975-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b975-111">Minimum supported server</span></span><br/> | <span data-ttu-id="3b975-112">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b975-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b975-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b975-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b975-114"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b975-114"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b975-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b975-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b975-116">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="3b975-116">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[<span data-ttu-id="3b975-117">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="3b975-117">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




