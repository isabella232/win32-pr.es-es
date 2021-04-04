---
title: Código de notificación de LVN_ODSTATECHANGED (commctrl. h)
description: Lo envía un control de vista de lista cuando el estado de un elemento o un intervalo de elementos ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- LVN_ODSTATECHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803062"
---
# <a name="lvn_odstatechanged-notification-code"></a><span data-ttu-id="c0d8b-105">Código de notificación de ODSTATECHANGED de LVN \_</span><span class="sxs-lookup"><span data-stu-id="c0d8b-105">LVN\_ODSTATECHANGED notification code</span></span>

<span data-ttu-id="c0d8b-106">Lo envía un control de vista de lista cuando el estado de un elemento o un intervalo de elementos ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c0d8b-106">Sent by a list-view control when the state of an item or range of items has changed.</span></span> <span data-ttu-id="c0d8b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c0d8b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c0d8b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0d8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0d8b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0d8b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0d8b-110">Puntero a una estructura [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) que contiene información sobre el elemento o los elementos que han cambiado.</span><span class="sxs-lookup"><span data-stu-id="c0d8b-110">Pointer to an [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) structure that contains information about the item or items that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0d8b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0d8b-111">Return value</span></span>

<span data-ttu-id="c0d8b-112">La aplicación que recibe este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="c0d8b-112">The application receiving this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0d8b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0d8b-113">Requirements</span></span>



| <span data-ttu-id="c0d8b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0d8b-114">Requirement</span></span> | <span data-ttu-id="c0d8b-115">Value</span><span class="sxs-lookup"><span data-stu-id="c0d8b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d8b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0d8b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d8b-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c0d8b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0d8b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0d8b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d8b-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0d8b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0d8b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0d8b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0d8b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0d8b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





