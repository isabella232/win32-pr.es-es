---
title: Código de notificación de LVN_GETINFOTIP (commctrl. h)
description: Se envía mediante una vista de iconos grandes control de vista de lista que tiene el \_ estilo extendido LVS ex previsor \_ .
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535644"
---
# <a name="lvn_getinfotip-notification-code"></a><span data-ttu-id="232bd-104">Código de notificación de GETINFOTIP de LVN \_</span><span class="sxs-lookup"><span data-stu-id="232bd-104">LVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="232bd-105">Se envía mediante una vista de iconos grandes control de vista de lista que tiene el estilo extendido [**LVS \_ ex \_**](extended-list-view-styles.md) previsor.</span><span class="sxs-lookup"><span data-stu-id="232bd-105">Sent by a large icon view list-view control that has the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="232bd-106">Este código de notificación se envía cuando el control de vista de lista solicita información de texto adicional que se va a mostrar en una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="232bd-106">This notification code is sent when the list-view control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="232bd-107">Se envía en forma de un mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="232bd-107">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a><span data-ttu-id="232bd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="232bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="232bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="232bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="232bd-110">Puntero a una estructura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="232bd-110">Pointer to an [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="232bd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="232bd-111">Return value</span></span>

<span data-ttu-id="232bd-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="232bd-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="232bd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="232bd-113">Remarks</span></span>

<span data-ttu-id="232bd-114">Este código de notificación solo lo envían los controles de vista de lista que tienen el estilo extendido [**LVS \_ ex \_**](extended-list-view-styles.md) previsor.</span><span class="sxs-lookup"><span data-stu-id="232bd-114">This notification code is only sent by list-view controls that have the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="232bd-115">El \_ código de notificación LVN GETINFOTIP se envía solo para el subelemento 0.</span><span class="sxs-lookup"><span data-stu-id="232bd-115">The LVN\_GETINFOTIP notification code is sent only for subitem 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="232bd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="232bd-116">Requirements</span></span>



| <span data-ttu-id="232bd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="232bd-117">Requirement</span></span> | <span data-ttu-id="232bd-118">Value</span><span class="sxs-lookup"><span data-stu-id="232bd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="232bd-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="232bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="232bd-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="232bd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="232bd-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="232bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="232bd-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="232bd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="232bd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="232bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="232bd-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="232bd-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="232bd-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="232bd-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="232bd-126">**LVN \_ GETINFOTIPW** (Unicode) y **LVN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="232bd-126">**LVN\_GETINFOTIPW** (Unicode) and **LVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





