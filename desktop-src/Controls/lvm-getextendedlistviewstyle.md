---
title: Mensaje de LVM_GETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Obtiene los estilos extendidos que están actualmente en uso para un control de vista de lista determinado. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetExtendedListViewStyle de ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078867"
---
# <a name="lvm_getextendedlistviewstyle-message"></a><span data-ttu-id="f74e3-105">\_Mensaje GETEXTENDEDLISTVIEWSTYLE LVM</span><span class="sxs-lookup"><span data-stu-id="f74e3-105">LVM\_GETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="f74e3-106">Obtiene los estilos extendidos que están actualmente en uso para un control de vista de lista determinado.</span><span class="sxs-lookup"><span data-stu-id="f74e3-106">Gets the extended styles that are currently in use for a given list-view control.</span></span> <span data-ttu-id="f74e3-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetExtendedListViewStyle de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .</span><span class="sxs-lookup"><span data-stu-id="f74e3-107">You can send this message explicitly or use the [**ListView\_GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f74e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f74e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f74e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f74e3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f74e3-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f74e3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f74e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f74e3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f74e3-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f74e3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f74e3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f74e3-113">Return value</span></span>

<span data-ttu-id="f74e3-114">Devuelve un **valor DWORD** que representa los estilos actualmente en uso para un determinado control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="f74e3-114">Returns a **DWORD** that represents the styles currently in use for a given list-view control.</span></span> <span data-ttu-id="f74e3-115">Este valor puede ser una combinación de [estilos de List-View extendidos](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f74e3-115">This value can be a combination of [Extended List-View Styles](extended-list-view-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f74e3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f74e3-116">Requirements</span></span>



| <span data-ttu-id="f74e3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f74e3-117">Requirement</span></span> | <span data-ttu-id="f74e3-118">Value</span><span class="sxs-lookup"><span data-stu-id="f74e3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f74e3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f74e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f74e3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f74e3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f74e3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f74e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f74e3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f74e3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f74e3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f74e3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f74e3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f74e3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





