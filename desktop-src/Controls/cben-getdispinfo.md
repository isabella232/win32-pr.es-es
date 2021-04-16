---
title: Código de notificación de CBEN_GETDISPINFO (commctrl. h)
description: Se envía para recuperar información de visualización sobre un elemento de devolución de llamada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533771"
---
# <a name="cben_getdispinfo-notification-code"></a><span data-ttu-id="8aee2-105">Código de notificación de GETDISPINFO de CBEN \_</span><span class="sxs-lookup"><span data-stu-id="8aee2-105">CBEN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="8aee2-106">Se envía para recuperar información de visualización sobre un elemento de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8aee2-106">Sent to retrieve display information about a callback item.</span></span> <span data-ttu-id="8aee2-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8aee2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8aee2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8aee2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aee2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8aee2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8aee2-110">Puntero a una estructura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="8aee2-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aee2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8aee2-111">Return value</span></span>

<span data-ttu-id="8aee2-112">El procesamiento de la aplicación en este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="8aee2-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aee2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8aee2-113">Remarks</span></span>

<span data-ttu-id="8aee2-114">La estructura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contiene una estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="8aee2-114">The [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure contains a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="8aee2-115">El miembro **Mask** especifica la información que solicita el control.</span><span class="sxs-lookup"><span data-stu-id="8aee2-115">The **mask** member specifies the information being requested by the control.</span></span>

<span data-ttu-id="8aee2-116">Rellene los miembros adecuados de la estructura para devolver la información solicitada al control.</span><span class="sxs-lookup"><span data-stu-id="8aee2-116">Fill the appropriate members of the structure to return the requested information to the control.</span></span> <span data-ttu-id="8aee2-117">Si el controlador de mensajes establece el miembro de **máscara** de la estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) en CBEIF \_ di \_ SETITEM, el control almacena la información y no la volverá a solicitar.</span><span class="sxs-lookup"><span data-stu-id="8aee2-117">If your message handler sets the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM, the control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aee2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aee2-118">Requirements</span></span>



| <span data-ttu-id="8aee2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aee2-119">Requirement</span></span> | <span data-ttu-id="8aee2-120">Value</span><span class="sxs-lookup"><span data-stu-id="8aee2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8aee2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8aee2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8aee2-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8aee2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8aee2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8aee2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8aee2-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8aee2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8aee2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8aee2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aee2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aee2-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8aee2-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8aee2-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8aee2-128">**CBEN \_ GETDISPINFOW** (Unicode) y **CBEN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8aee2-128">**CBEN\_GETDISPINFOW** (Unicode) and **CBEN\_GETDISPINFOA** (ANSI)</span></span><br/>         |



 

 





