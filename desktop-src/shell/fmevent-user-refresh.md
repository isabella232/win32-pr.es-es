---
description: Se envía a un archivo DLL de extensión cuando el usuario elige el comando actualizar en el menú Ver del administrador de archivos. La extensión puede usar esta notificación para actualizar el menú.
title: Mensaje de FMEVENT_USER_REFRESH (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: c3c4596b0ea589545c6e59953b9c7b5977e07b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985511"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="398e9-104">Mensaje de actualización de \_ usuario de FMEVENT \_</span><span class="sxs-lookup"><span data-stu-id="398e9-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="398e9-105">Se envía a un archivo DLL de extensión cuando el usuario elige el comando **Actualizar** en el menú **Ver** del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="398e9-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="398e9-106">La extensión puede usar esta notificación para actualizar el menú.</span><span class="sxs-lookup"><span data-stu-id="398e9-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="398e9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="398e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="398e9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="398e9-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="398e9-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="398e9-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="398e9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="398e9-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="398e9-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="398e9-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="398e9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="398e9-112">Return value</span></span>

<span data-ttu-id="398e9-113">Un archivo DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="398e9-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="398e9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="398e9-114">Requirements</span></span>



| <span data-ttu-id="398e9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="398e9-115">Requirement</span></span> | <span data-ttu-id="398e9-116">Value</span><span class="sxs-lookup"><span data-stu-id="398e9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="398e9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="398e9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="398e9-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="398e9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="398e9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="398e9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="398e9-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="398e9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="398e9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="398e9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="398e9-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="398e9-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="398e9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="398e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398e9-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="398e9-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




