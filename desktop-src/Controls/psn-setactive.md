---
title: Código de notificación de PSN_SETACTIVE (Prsht. h)
description: Notifica a una página que está a punto de activarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996640"
---
# <a name="psn_setactive-notification-code"></a><span data-ttu-id="0dc4a-105">Código de notificación de SETACTIVE de PSN \_</span><span class="sxs-lookup"><span data-stu-id="0dc4a-105">PSN\_SETACTIVE notification code</span></span>

<span data-ttu-id="0dc4a-106">Notifica a una página que está a punto de activarse.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-106">Notifies a page that it is about to be activated.</span></span> <span data-ttu-id="0dc4a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0dc4a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0dc4a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0dc4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc4a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0dc4a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0dc4a-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="0dc4a-111">Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="0dc4a-112">El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc4a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0dc4a-113">Return value</span></span>

<span data-ttu-id="0dc4a-114">Devuelve cero para aceptar la activación, o-1 para activar la página siguiente o anterior (en función de si el usuario hizo clic en el botón **siguiente** o **atrás** ).</span><span class="sxs-lookup"><span data-stu-id="0dc4a-114">Returns zero to accept the activation, or -1 to activate the next or the previous page (depending on whether the user clicked the **Next** or **Back** button).</span></span> <span data-ttu-id="0dc4a-115">Para establecer la activación en una página determinada, devuelva el identificador de recursos de la página.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-115">To set the activation to a particular page, return the resource identifier of the page.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc4a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dc4a-116">Remarks</span></span>

<span data-ttu-id="0dc4a-117">El \_ código de notificación SETACTIVE de PSN se envía antes de que la página esté visible.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-117">The PSN\_SETACTIVE notification code is sent before the page is visible.</span></span> <span data-ttu-id="0dc4a-118">Una aplicación puede utilizar este código de notificación para inicializar los datos en la página.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-118">An application can use this notification code to initialize data in the page.</span></span>

> [!Note]  
> <span data-ttu-id="0dc4a-119">La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación SETACTIVE de PSN.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-119">The property sheet is in the process of manipulating the list of pages when the PSN\_SETACTIVE notification code is sent.</span></span> <span data-ttu-id="0dc4a-120">No intente agregar, quitar o insertar páginas mientras controla este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="0dc4a-121">Si lo hace, tendrá resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="0dc4a-122">Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT y el procedimiento de cuadro de diálogo debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="0dc4a-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc4a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc4a-123">Requirements</span></span>



| <span data-ttu-id="0dc4a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc4a-124">Requirement</span></span> | <span data-ttu-id="0dc4a-125">Value</span><span class="sxs-lookup"><span data-stu-id="0dc4a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc4a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dc4a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc4a-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0dc4a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0dc4a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dc4a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc4a-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0dc4a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0dc4a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dc4a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dc4a-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc4a-131"><dt>Prsht.h</dt></span></span> </dl> |



 

