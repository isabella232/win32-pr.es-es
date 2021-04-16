---
title: Código de notificación de RBN_AUTOSIZE (commctrl. h)
description: Enviado por un control rebar creado con el estilo de tamaño automático de RBS \_ cuando el rebar cambia automáticamente de tamaño. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658388"
---
# <a name="rbn_autosize-notification-code"></a><span data-ttu-id="1c977-105">RBN \_ código de notificación de tamaño automático</span><span class="sxs-lookup"><span data-stu-id="1c977-105">RBN\_AUTOSIZE notification code</span></span>

<span data-ttu-id="1c977-106">Enviado por un control rebar creado con el estilo de [**\_ tamaño**](rebar-control-styles.md) automático de RBS cuando el rebar cambia automáticamente de tamaño.</span><span class="sxs-lookup"><span data-stu-id="1c977-106">Sent by a rebar control created with the [**RBS\_AUTOSIZE**](rebar-control-styles.md) style when the rebar automatically resizes itself.</span></span> <span data-ttu-id="1c977-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1c977-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1c977-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c977-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c977-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c977-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c977-110">Puntero a una estructura [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) que contiene información sobre la operación de cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="1c977-110">Pointer to an [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) structure that contains information about the resize operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c977-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c977-111">Return value</span></span>

<span data-ttu-id="1c977-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="1c977-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c977-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c977-113">Requirements</span></span>



| <span data-ttu-id="1c977-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c977-114">Requirement</span></span> | <span data-ttu-id="1c977-115">Value</span><span class="sxs-lookup"><span data-stu-id="1c977-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c977-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c977-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c977-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1c977-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c977-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c977-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c977-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c977-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c977-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c977-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c977-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c977-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





