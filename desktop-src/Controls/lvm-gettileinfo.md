---
title: Mensaje de LVM_GETTILEINFO (commctrl. h)
description: Recupera información sobre un icono en un control de vista de lista.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- LVM_GETTILEINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079651"
---
# <a name="lvm_gettileinfo-message"></a><span data-ttu-id="f080a-104">\_Mensaje GETTILEINFO LVM</span><span class="sxs-lookup"><span data-stu-id="f080a-104">LVM\_GETTILEINFO message</span></span>

<span data-ttu-id="f080a-105">Recupera información sobre un icono en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="f080a-105">Retrieves information about a tile in a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f080a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f080a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f080a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f080a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f080a-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f080a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f080a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f080a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f080a-110">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> que recibe la información recuperada.</span><span class="sxs-lookup"><span data-stu-id="f080a-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f080a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f080a-111">Return value</span></span>

<span data-ttu-id="f080a-112">No se usa el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f080a-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f080a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f080a-113">Remarks</span></span>

<span data-ttu-id="f080a-114">La vista en mosaico es una nueva forma de organizar y mostrar elementos en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="f080a-114">Tile view is a new way of arranging and displaying items in a list-view control.</span></span> <span data-ttu-id="f080a-115">Las demás vistas son el icono, el icono pequeño, los detalles y la lista.</span><span class="sxs-lookup"><span data-stu-id="f080a-115">The other views are icon, small icon, details, and list.</span></span>

> [!Note]  
> <span data-ttu-id="f080a-116">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="f080a-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f080a-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f080a-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f080a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f080a-118">Requirements</span></span>



| <span data-ttu-id="f080a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f080a-119">Requirement</span></span> | <span data-ttu-id="f080a-120">Value</span><span class="sxs-lookup"><span data-stu-id="f080a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f080a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f080a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f080a-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f080a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f080a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f080a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f080a-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f080a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f080a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f080a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f080a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f080a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





