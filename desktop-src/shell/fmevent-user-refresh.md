---
description: Se envía a un archivo DLL de extensión cuando el usuario elige el comando Actualizar en el menú Ver del Administrador de archivos. La extensión puede usar esta notificación para actualizar su menú.
title: FMEVENT_USER_REFRESH mensaje (Wfext.h)
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
ms.openlocfilehash: 16f75f562149b50237a6b41bf2023d1f694741e3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841266"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="7bec8-104">Mensaje DE ACTUALIZACIÓN \_ DE USUARIO DE FMEVENT \_</span><span class="sxs-lookup"><span data-stu-id="7bec8-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="7bec8-105">Se envía a un archivo DLL de extensión cuando el usuario elige el **comando Actualizar** en el **menú** Ver del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="7bec8-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="7bec8-106">La extensión puede usar esta notificación para actualizar su menú.</span><span class="sxs-lookup"><span data-stu-id="7bec8-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="7bec8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7bec8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bec8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7bec8-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7bec8-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7bec8-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7bec8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7bec8-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7bec8-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7bec8-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bec8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bec8-112">Return value</span></span>

<span data-ttu-id="7bec8-113">Un archivo DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7bec8-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bec8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bec8-114">Requirements</span></span>



| <span data-ttu-id="7bec8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bec8-115">Requirement</span></span> | <span data-ttu-id="7bec8-116">Value</span><span class="sxs-lookup"><span data-stu-id="7bec8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7bec8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bec8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7bec8-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7bec8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7bec8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bec8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7bec8-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bec8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7bec8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bec8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bec8-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="7bec8-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bec8-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7bec8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bec8-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="7bec8-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




