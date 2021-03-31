---
title: Mensaje de SBM_GETSCROLLBARINFO (Winuser. h)
description: Lo envía una aplicación para recuperar información sobre la barra de desplazamiento especificada.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- SBM_GETSCROLLBARINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802180"
---
# <a name="sbm_getscrollbarinfo-message"></a><span data-ttu-id="cab32-104">\_Mensaje GETSCROLLBARINFO SBM</span><span class="sxs-lookup"><span data-stu-id="cab32-104">SBM\_GETSCROLLBARINFO message</span></span>

<span data-ttu-id="cab32-105">Lo envía una aplicación para recuperar información sobre la barra de desplazamiento especificada.</span><span class="sxs-lookup"><span data-stu-id="cab32-105">Sent by an application to retrieve information about the specified scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="cab32-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cab32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cab32-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cab32-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cab32-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cab32-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cab32-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cab32-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cab32-110">Puntero a una estructura [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) que recibe la información.</span><span class="sxs-lookup"><span data-stu-id="cab32-110">Pointer to a [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cab32-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cab32-111">Return value</span></span>

<span data-ttu-id="cab32-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="cab32-112">Returns nonzero if successful or zero otherwise.</span></span>

<span data-ttu-id="cab32-113">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cab32-113">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="cab32-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cab32-114">Requirements</span></span>



| <span data-ttu-id="cab32-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cab32-115">Requirement</span></span> | <span data-ttu-id="cab32-116">Value</span><span class="sxs-lookup"><span data-stu-id="cab32-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cab32-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cab32-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cab32-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cab32-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cab32-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cab32-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cab32-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cab32-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cab32-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cab32-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cab32-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cab32-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab32-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cab32-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="cab32-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cab32-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cab32-125">**GetScrollBarInfo**</span><span class="sxs-lookup"><span data-stu-id="cab32-125">**GetScrollBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[<span data-ttu-id="cab32-126">**SCROLLBARINFO**</span><span class="sxs-lookup"><span data-stu-id="cab32-126">**SCROLLBARINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

