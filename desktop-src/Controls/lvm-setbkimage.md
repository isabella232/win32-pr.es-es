---
title: Mensaje de LVM_SETBKIMAGE (commctrl. h)
description: Establece la imagen de fondo en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetBkImage de ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- LVM_SETBKIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491458"
---
# <a name="lvm_setbkimage-message"></a><span data-ttu-id="5b4be-105">\_Mensaje SETBKIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="5b4be-105">LVM\_SETBKIMAGE message</span></span>

<span data-ttu-id="5b4be-106">Establece la imagen de fondo en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5b4be-106">Sets the background image in a list-view control.</span></span> <span data-ttu-id="5b4be-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetBkImage de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .</span><span class="sxs-lookup"><span data-stu-id="5b4be-107">You can send this message explicitly or by using the [**ListView\_SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b4be-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b4be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b4be-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b4be-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b4be-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5b4be-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5b4be-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b4be-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b4be-112">Puntero a una estructura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que contiene la nueva información de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="5b4be-112">Pointer to a [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that contains the new background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b4be-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b4be-113">Return value</span></span>

<span data-ttu-id="5b4be-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="5b4be-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="5b4be-115">Devuelve cero si el miembro **ulFlags** de la estructura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) es **LVBKIF \_ source \_ None**.</span><span class="sxs-lookup"><span data-stu-id="5b4be-115">Returns zero if the **ulFlags** member of the [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure is **LVBKIF\_SOURCE\_NONE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b4be-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b4be-116">Remarks</span></span>

<span data-ttu-id="5b4be-117">Dado que el control de vista de lista utiliza OLE COM para manipular las imágenes de fondo, la aplicación que realiza la llamada debe llamar a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5b4be-117">Because the list-view control uses OLE COM to manipulate the background images, the calling application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before sending this message.</span></span> <span data-ttu-id="5b4be-118">Es mejor llamar a una de estas funciones cuando se inicializa la aplicación y llamar a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) o [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) cuando la aplicación está finalizando.</span><span class="sxs-lookup"><span data-stu-id="5b4be-118">It is best to call one of these functions when the application is initialized and call either [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) or [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) when the application is terminating.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b4be-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b4be-119">Requirements</span></span>



| <span data-ttu-id="5b4be-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b4be-120">Requirement</span></span> | <span data-ttu-id="5b4be-121">Value</span><span class="sxs-lookup"><span data-stu-id="5b4be-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4be-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b4be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b4be-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5b4be-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b4be-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b4be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b4be-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b4be-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b4be-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b4be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b4be-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b4be-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5b4be-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5b4be-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5b4be-129">**LVM \_ SETBKIMAGEW** (Unicode) y **\_ SETBKIMAGEA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5b4be-129">**LVM\_SETBKIMAGEW** (Unicode) and **LVM\_SETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5b4be-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b4be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b4be-131">**\_GETBKIMAGE LVM**</span><span class="sxs-lookup"><span data-stu-id="5b4be-131">**LVM\_GETBKIMAGE**</span></span>](lvm-getbkimage.md)
</dt> </dl>

 

