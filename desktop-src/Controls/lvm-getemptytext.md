---
title: Mensaje de LVM_GETEMPTYTEXT (commctrl. h)
description: Obtiene el texto destinado a mostrarse cuando el control de vista de lista aparece vacío. Envíe este mensaje explícitamente o mediante la \_ macro GetEmptyText de ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489059"
---
# <a name="lvm_getemptytext-message"></a><span data-ttu-id="b94c6-105">\_Mensaje GETEMPTYTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="b94c6-105">LVM\_GETEMPTYTEXT message</span></span>

<span data-ttu-id="b94c6-106">Obtiene el texto destinado a mostrarse cuando el control de vista de lista aparece vacío.</span><span class="sxs-lookup"><span data-stu-id="b94c6-106">Gets the text meant for display when the list-view control appears empty.</span></span> <span data-ttu-id="b94c6-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetEmptyText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .</span><span class="sxs-lookup"><span data-stu-id="b94c6-107">Send this message explicitly or by using the [**ListView\_GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b94c6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b94c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b94c6-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b94c6-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b94c6-110">Tamaño del búfer al que apunta *lParam*, incluido el **valor null** final.</span><span class="sxs-lookup"><span data-stu-id="b94c6-110">The size of the buffer pointed to by *lParam*, including the terminating **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b94c6-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b94c6-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b94c6-112">Un puntero a un búfer Unicode de terminación null de tamaño especificado por *wParam* para recibir el texto.</span><span class="sxs-lookup"><span data-stu-id="b94c6-112">A pointer to a null-terminated, Unicode buffer of size specified by *wParam* to receive the text.</span></span> <span data-ttu-id="b94c6-113">El autor de la llamada es responsable de la asignación del búfer.</span><span class="sxs-lookup"><span data-stu-id="b94c6-113">The caller is responsible for allocating the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b94c6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b94c6-114">Return value</span></span>

<span data-ttu-id="b94c6-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b94c6-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b94c6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b94c6-116">Requirements</span></span>



| <span data-ttu-id="b94c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b94c6-117">Requirement</span></span> | <span data-ttu-id="b94c6-118">Value</span><span class="sxs-lookup"><span data-stu-id="b94c6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b94c6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b94c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b94c6-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b94c6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b94c6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b94c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b94c6-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b94c6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b94c6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b94c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b94c6-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b94c6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





