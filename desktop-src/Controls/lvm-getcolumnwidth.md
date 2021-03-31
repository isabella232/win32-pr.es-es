---
title: Mensaje de LVM_GETCOLUMNWIDTH (commctrl. h)
description: Obtiene el ancho de una columna en la vista de lista o informe. Puede enviar este mensaje explícitamente o mediante la \_ macro GetColumnWidth de ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149903"
---
# <a name="lvm_getcolumnwidth-message"></a><span data-ttu-id="a7dab-105">\_Mensaje GETCOLUMNWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="a7dab-105">LVM\_GETCOLUMNWIDTH message</span></span>

<span data-ttu-id="a7dab-106">Obtiene el ancho de una columna en la vista de lista o informe.</span><span class="sxs-lookup"><span data-stu-id="a7dab-106">Gets the width of a column in report or list view.</span></span> <span data-ttu-id="a7dab-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetColumnWidth de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="a7dab-107">You can send this message explicitly or by using the [**ListView\_GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7dab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7dab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7dab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7dab-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7dab-110">Índice de la columna.</span><span class="sxs-lookup"><span data-stu-id="a7dab-110">The index of the column.</span></span> <span data-ttu-id="a7dab-111">Este parámetro se omite en la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="a7dab-111">This parameter is ignored in list view.</span></span>

</dd> <dt>

<span data-ttu-id="a7dab-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7dab-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a7dab-113">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a7dab-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7dab-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7dab-114">Return value</span></span>

<span data-ttu-id="a7dab-115">Devuelve el ancho de columna si se realiza correctamente o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a7dab-115">Returns the column width if successful, or zero otherwise.</span></span> <span data-ttu-id="a7dab-116">Si este mensaje se envía a un control de vista de lista con el estilo de [**\_ Informe LVS**](list-view-window-styles.md) y la columna especificada no existe, el valor devuelto es indefinido.</span><span class="sxs-lookup"><span data-stu-id="a7dab-116">If this message is sent to a list-view control with the [**LVS\_REPORT**](list-view-window-styles.md) style and the specified column does not exist, the return value is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7dab-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7dab-117">Requirements</span></span>



| <span data-ttu-id="a7dab-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7dab-118">Requirement</span></span> | <span data-ttu-id="a7dab-119">Value</span><span class="sxs-lookup"><span data-stu-id="a7dab-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7dab-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7dab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7dab-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a7dab-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7dab-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7dab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7dab-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7dab-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7dab-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7dab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7dab-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7dab-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





