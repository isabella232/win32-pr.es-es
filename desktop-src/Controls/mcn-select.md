---
title: Código de notificación de MCN_SELECT (commctrl. h)
description: Se envía por un control de calendario mensual cuando el usuario realiza una selección de fecha explícita dentro de un control de calendario mensual. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079003"
---
# <a name="mcn_select-notification-code"></a><span data-ttu-id="0db1d-105">MCN \_ seleccionar código de notificación</span><span class="sxs-lookup"><span data-stu-id="0db1d-105">MCN\_SELECT notification code</span></span>

<span data-ttu-id="0db1d-106">Se envía por un control de calendario mensual cuando el usuario realiza una selección de fecha explícita dentro de un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="0db1d-106">Sent by a month calendar control when the user makes an explicit date selection within a month calendar control.</span></span> <span data-ttu-id="0db1d-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0db1d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0db1d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0db1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0db1d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0db1d-110">Puntero a una estructura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contiene información sobre el intervalo de fechas seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="0db1d-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db1d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0db1d-111">Return value</span></span>

<span data-ttu-id="0db1d-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0db1d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0db1d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0db1d-113">Remarks</span></span>

<span data-ttu-id="0db1d-114">El código de notificación **\_ Select MCN** es similar a [**MCN \_ SELCHANGE**](mcn-selchange.md), pero **MCN \_ Select** solo se envía como respuesta a las selecciones de fecha explícitas de un usuario.</span><span class="sxs-lookup"><span data-stu-id="0db1d-114">The **MCN\_SELECT** notification code is similar to [**MCN\_SELCHANGE**](mcn-selchange.md), but **MCN\_SELECT** is sent only in response to a user's explicit date selections.</span></span> <span data-ttu-id="0db1d-115">**MCN \_ SELCHANGE** se aplica a cualquier cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="0db1d-115">**MCN\_SELCHANGE** applies to any selection change.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db1d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0db1d-116">Requirements</span></span>



| <span data-ttu-id="0db1d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db1d-117">Requirement</span></span> | <span data-ttu-id="0db1d-118">Value</span><span class="sxs-lookup"><span data-stu-id="0db1d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0db1d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db1d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0db1d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0db1d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0db1d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db1d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0db1d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0db1d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0db1d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0db1d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db1d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db1d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





