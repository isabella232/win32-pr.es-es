---
title: Código de notificación de PSN_HELP (Prsht. h)
description: Notifica a una página que el usuario ha haga clic en el botón ayuda. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- PSN_HELP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658233"
---
# <a name="psn_help-notification-code"></a><span data-ttu-id="19581-105">Código de notificación de ayuda de PSN \_</span><span class="sxs-lookup"><span data-stu-id="19581-105">PSN\_HELP notification code</span></span>

<span data-ttu-id="19581-106">Notifica a una página que el usuario ha haga clic en el botón ayuda.</span><span class="sxs-lookup"><span data-stu-id="19581-106">Notifies a page that the user has clicked the Help button.</span></span> <span data-ttu-id="19581-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="19581-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="19581-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19581-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19581-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19581-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19581-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="19581-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="19581-111">Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="19581-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="19581-112">El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.</span><span class="sxs-lookup"><span data-stu-id="19581-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19581-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19581-113">Return value</span></span>

<span data-ttu-id="19581-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="19581-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19581-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19581-115">Remarks</span></span>

<span data-ttu-id="19581-116">Una aplicación debe mostrar información de ayuda de la página.</span><span class="sxs-lookup"><span data-stu-id="19581-116">An application should display Help information for the page.</span></span>

> [!Note]  
> <span data-ttu-id="19581-117">Este código de notificación no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="19581-117">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="19581-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19581-118">Requirements</span></span>



| <span data-ttu-id="19581-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="19581-119">Requirement</span></span> | <span data-ttu-id="19581-120">Value</span><span class="sxs-lookup"><span data-stu-id="19581-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19581-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19581-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19581-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19581-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19581-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19581-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19581-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="19581-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="19581-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19581-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="19581-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="19581-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





