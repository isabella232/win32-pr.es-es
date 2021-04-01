---
title: Mensaje de TB_GETBITMAPFLAGS (commctrl. h)
description: Recupera las marcas que describen el tipo de mapa de bits que se va a utilizar.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- TB_GETBITMAPFLAGS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151260"
---
# <a name="tb_getbitmapflags-message"></a><span data-ttu-id="8eecf-104">\_Mensaje GETBITMAPFLAGS TB</span><span class="sxs-lookup"><span data-stu-id="8eecf-104">TB\_GETBITMAPFLAGS message</span></span>

<span data-ttu-id="8eecf-105">Recupera las marcas que describen el tipo de mapa de bits que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="8eecf-105">Retrieves the flags that describe the type of bitmap to be used.</span></span>

## <a name="parameters"></a><span data-ttu-id="8eecf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8eecf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eecf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8eecf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8eecf-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8eecf-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8eecf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8eecf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8eecf-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8eecf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eecf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8eecf-111">Return value</span></span>

<span data-ttu-id="8eecf-112">Devuelve un valor **DWORD** que describe el tipo de mapa de bits que se debe usar.</span><span class="sxs-lookup"><span data-stu-id="8eecf-112">Returns a **DWORD** value that describes the type of bitmap that should be used.</span></span> <span data-ttu-id="8eecf-113">Si el valor devuelto tiene \_ establecida la marca grande TBBF, las aplicaciones deben usar mapas de bits grandes (24 x 24); de lo contrario, las aplicaciones deben usar mapas de bits pequeños (16 x 16).</span><span class="sxs-lookup"><span data-stu-id="8eecf-113">If this return value has the TBBF\_LARGE flag set, applications should use large bitmaps (24 x 24); otherwise, applications should use small bitmaps (16 x 16).</span></span> <span data-ttu-id="8eecf-114">Todos los demás bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="8eecf-114">All other bits are reserved.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eecf-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8eecf-115">Remarks</span></span>

<span data-ttu-id="8eecf-116">El valor devuelto por **TB \_ GETBITMAPFLAGS** solo es un aviso.</span><span class="sxs-lookup"><span data-stu-id="8eecf-116">The value returned by **TB\_GETBITMAPFLAGS** is only advisory.</span></span> <span data-ttu-id="8eecf-117">El control de barra de herramientas recomienda mapas de bits grandes o pequeños en función de si el usuario ha elegido fuentes grandes o pequeñas.</span><span class="sxs-lookup"><span data-stu-id="8eecf-117">The toolbar control recommends large or small bitmaps based upon whether the user has chosen large or small fonts.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eecf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eecf-118">Requirements</span></span>



| <span data-ttu-id="8eecf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eecf-119">Requirement</span></span> | <span data-ttu-id="8eecf-120">Value</span><span class="sxs-lookup"><span data-stu-id="8eecf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8eecf-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8eecf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8eecf-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8eecf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8eecf-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8eecf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8eecf-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8eecf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8eecf-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8eecf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eecf-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eecf-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





