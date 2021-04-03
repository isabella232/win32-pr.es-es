---
title: Mensaje de LVM_GETOUTLINECOLOR (commctrl. h)
description: Recupera el color del borde de un control de vista de lista si \_ \_ se establece el estilo de ventana extendida LVS ex BORDERSELECT.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- LVM_GETOUTLINECOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905505"
---
# <a name="lvm_getoutlinecolor-message"></a><span data-ttu-id="80205-104">\_Mensaje GETOUTLINECOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="80205-104">LVM\_GETOUTLINECOLOR message</span></span>

<span data-ttu-id="80205-105">Recupera el color del borde de un control de vista de lista si se establece el estilo de ventana extendida [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="80205-105">Retrieves the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="80205-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80205-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80205-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80205-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="80205-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="80205-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="80205-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80205-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="80205-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="80205-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80205-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80205-111">Return value</span></span>

<span data-ttu-id="80205-112">Devuelve una estructura **COLORREF** que contiene el color del borde de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="80205-112">Returns a **COLORREF** structure that contains the color of the border of a list-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="80205-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80205-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="80205-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="80205-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="80205-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="80205-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80205-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80205-116">Requirements</span></span>



| <span data-ttu-id="80205-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="80205-117">Requirement</span></span> | <span data-ttu-id="80205-118">Value</span><span class="sxs-lookup"><span data-stu-id="80205-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80205-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80205-119">Minimum supported client</span></span><br/> | <span data-ttu-id="80205-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="80205-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80205-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80205-121">Minimum supported server</span></span><br/> | <span data-ttu-id="80205-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="80205-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80205-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80205-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="80205-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="80205-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





