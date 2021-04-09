---
title: Mensaje de RB_HITTEST (commctrl. h)
description: Determina qué parte de una banda rebar se encuentra en un punto determinado de la pantalla, si existe una banda rebar en ese punto.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078929"
---
# <a name="rb_hittest-message"></a><span data-ttu-id="d999b-104">Mensaje de RB \_ HITTEST</span><span class="sxs-lookup"><span data-stu-id="d999b-104">RB\_HITTEST message</span></span>

<span data-ttu-id="d999b-105">Determina qué parte de una banda rebar se encuentra en un punto determinado de la pantalla, si existe una banda rebar en ese punto.</span><span class="sxs-lookup"><span data-stu-id="d999b-105">Determines which portion of a rebar band is at a given point on the screen, if a rebar band exists at that point.</span></span>

## <a name="parameters"></a><span data-ttu-id="d999b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d999b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d999b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d999b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d999b-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d999b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d999b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d999b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d999b-110">Puntero a una estructura [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="d999b-110">Pointer to an [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) structure.</span></span> <span data-ttu-id="d999b-111">Antes de enviar el mensaje, el miembro **PT** de esta estructura se debe inicializar en el punto en el que se realizará la prueba de posicionamiento, en coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="d999b-111">Before sending the message, the **pt** member of this structure must be initialized to the point that will be hit tested, in client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d999b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d999b-112">Return value</span></span>

<span data-ttu-id="d999b-113">Devuelve el índice de base cero de la banda en el punto especificado, o-1 si no hay ninguna banda rebar en el punto.</span><span class="sxs-lookup"><span data-stu-id="d999b-113">Returns the zero-based index of the band at the given point, or -1 if no rebar band was at the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="d999b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d999b-114">Requirements</span></span>



| <span data-ttu-id="d999b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d999b-115">Requirement</span></span> | <span data-ttu-id="d999b-116">Value</span><span class="sxs-lookup"><span data-stu-id="d999b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d999b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d999b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d999b-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d999b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d999b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d999b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d999b-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d999b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d999b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d999b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d999b-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d999b-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





