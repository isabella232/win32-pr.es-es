---
title: Mensaje de CCM_GETVERSION (commctrl. h)
description: Obtiene el número de versión de un control establecido por el mensaje de SETVERSION de CCM más reciente \_ .
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150563"
---
# <a name="ccm_getversion-message"></a><span data-ttu-id="41926-104">\_Mensaje GETVERSION de CCM</span><span class="sxs-lookup"><span data-stu-id="41926-104">CCM\_GETVERSION message</span></span>

<span data-ttu-id="41926-105">Obtiene el número de versión de un control establecido por el mensaje [**de \_ SETVERSION de CCM**](ccm-setversion.md) más reciente.</span><span class="sxs-lookup"><span data-stu-id="41926-105">Gets the version number for a control set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="41926-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41926-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41926-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41926-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="41926-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="41926-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="41926-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41926-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="41926-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="41926-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41926-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41926-111">Return value</span></span>

<span data-ttu-id="41926-112">Devuelve el número de versión establecido por el mensaje [**de \_ SETVERSION de CCM**](ccm-setversion.md) más reciente.</span><span class="sxs-lookup"><span data-stu-id="41926-112">Returns the version number set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="41926-113">Si no se ha enviado ningún mensaje de este tipo, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="41926-113">If no such message has been sent, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="41926-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41926-114">Remarks</span></span>

<span data-ttu-id="41926-115">Este mensaje no devuelve la versión del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="41926-115">This message does not return the DLL version.</span></span> <span data-ttu-id="41926-116">Consulte [versiones de Shell](common-control-versions.md) para obtener una explicación de cómo usar [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para recuperar la versión de dll actual.</span><span class="sxs-lookup"><span data-stu-id="41926-116">See [Shell Versions](common-control-versions.md) for a discussion of how to use [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) to retrieve the current DLL version.</span></span>

> [!Note]  
> <span data-ttu-id="41926-117">El número de versión se establece en un control según el control y puede no ser el mismo para todos los controles.</span><span class="sxs-lookup"><span data-stu-id="41926-117">The version number is set on a control by control basis, and may not be the same for all controls.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41926-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41926-118">Requirements</span></span>



| <span data-ttu-id="41926-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="41926-119">Requirement</span></span> | <span data-ttu-id="41926-120">Value</span><span class="sxs-lookup"><span data-stu-id="41926-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41926-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41926-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41926-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="41926-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41926-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41926-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41926-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="41926-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41926-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41926-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="41926-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41926-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

