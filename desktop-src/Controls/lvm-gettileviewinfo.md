---
title: Mensaje de LVM_GETTILEVIEWINFO (commctrl. h)
description: Recupera información sobre un control de vista de lista en la vista de mosaico.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- LVM_GETTILEVIEWINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe1f34da560d539a9ae12cc7a065b2bf37bc3c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803386"
---
# <a name="lvm_gettileviewinfo-message"></a><span data-ttu-id="49ccf-104">\_Mensaje GETTILEVIEWINFO LVM</span><span class="sxs-lookup"><span data-stu-id="49ccf-104">LVM\_GETTILEVIEWINFO message</span></span>

<span data-ttu-id="49ccf-105">Recupera información sobre un control de vista de lista en la vista de mosaico.</span><span class="sxs-lookup"><span data-stu-id="49ccf-105">Retrieves information about a list-view control in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="49ccf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49ccf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ccf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49ccf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="49ccf-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="49ccf-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="49ccf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49ccf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="49ccf-110">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> que recibe la información recuperada.</span><span class="sxs-lookup"><span data-stu-id="49ccf-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ccf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49ccf-111">Return value</span></span>

<span data-ttu-id="49ccf-112">No se usa el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="49ccf-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="49ccf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49ccf-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49ccf-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="49ccf-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="49ccf-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="49ccf-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49ccf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ccf-116">Requirements</span></span>



| <span data-ttu-id="49ccf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ccf-117">Requirement</span></span> | <span data-ttu-id="49ccf-118">Value</span><span class="sxs-lookup"><span data-stu-id="49ccf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49ccf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ccf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="49ccf-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="49ccf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49ccf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ccf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="49ccf-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="49ccf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49ccf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49ccf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ccf-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49ccf-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





