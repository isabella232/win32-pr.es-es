---
title: Mensaje de LVM_GETGROUPINFOBYINDEX (commctrl. h)
description: Obtiene información sobre un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro GetGroupInfoByIndex de ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150545"
---
# <a name="lvm_getgroupinfobyindex-message"></a><span data-ttu-id="3b127-105">\_Mensaje GETGROUPINFOBYINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="3b127-105">LVM\_GETGROUPINFOBYINDEX message</span></span>

<span data-ttu-id="3b127-106">Obtiene información sobre un grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="3b127-106">Gets information on a specified group.</span></span> <span data-ttu-id="3b127-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetGroupInfoByIndex de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .</span><span class="sxs-lookup"><span data-stu-id="3b127-107">Send this message explicitly or by using the [**ListView\_GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b127-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b127-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b127-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b127-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b127-110">Índice del grupo.</span><span class="sxs-lookup"><span data-stu-id="3b127-110">The index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="3b127-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3b127-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b127-112">Puntero a una estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) para recibir información sobre el grupo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="3b127-112">A pointer to an [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="3b127-113">El proceso de llamada es responsable de la asignación de memoria para la estructura y los búferes de la estructura, como el que señala el miembro **pszHeader** .</span><span class="sxs-lookup"><span data-stu-id="3b127-113">The calling process is responsible for allocating memory for the structure and any buffers in the structure, such as the one pointed to by the **pszHeader** member.</span></span> <span data-ttu-id="3b127-114">Establezca los miembros contingentes de la estructura, como **cchHeader** el tamaño del búfer al que apunta **pszHeader** en **WCHARs** , incluido el **valor null** final.</span><span class="sxs-lookup"><span data-stu-id="3b127-114">Set any contingent members of the structure, such as **cchHeader** the size of the buffer pointed to by **pszHeader** in **WCHARs** including the terminating **NULL**.</span></span> <span data-ttu-id="3b127-115">Establezca **cbSize** en SIZEOF (LVGROUP).</span><span class="sxs-lookup"><span data-stu-id="3b127-115">Set **cbSize** to sizeof(LVGROUP).</span></span>

<span data-ttu-id="3b127-116">El receptor del mensaje es responsable de establecer los miembros de la estructura con información para el grupo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="3b127-116">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b127-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b127-117">Return value</span></span>

<span data-ttu-id="3b127-118">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3b127-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b127-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b127-119">Requirements</span></span>



| <span data-ttu-id="3b127-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b127-120">Requirement</span></span> | <span data-ttu-id="3b127-121">Value</span><span class="sxs-lookup"><span data-stu-id="3b127-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b127-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b127-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b127-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b127-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b127-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b127-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b127-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b127-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b127-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b127-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b127-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b127-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





