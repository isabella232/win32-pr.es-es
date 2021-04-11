---
description: Se envía cuando un usuario realiza un gesto de lápiz. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Mensaje de WM_TABLET_FLICK (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275358"
---
# <a name="wm_tablet_flick-message"></a><span data-ttu-id="c6b22-104">\_Mensaje de gesto de Tablet PC de WM \_</span><span class="sxs-lookup"><span data-stu-id="c6b22-104">WM\_TABLET\_FLICK message</span></span>

<span data-ttu-id="c6b22-105">Se envía cuando un usuario realiza un gesto de lápiz.</span><span class="sxs-lookup"><span data-stu-id="c6b22-105">Sent when a user performs a pen flick.</span></span> <span data-ttu-id="c6b22-106">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c6b22-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a><span data-ttu-id="c6b22-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6b22-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b22-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6b22-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b22-109">Una [**\_ estructura de datos de gestos**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) que contiene información sobre el gesto de lápiz que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="c6b22-109">A [**FLICK\_DATA Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) that contains information about the pen flick that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c6b22-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6b22-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b22-111">La [**\_ estructura de punto de gesto**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) que especifica dónde se produjo el gesto de lápiz.</span><span class="sxs-lookup"><span data-stu-id="c6b22-111">The [**FLICK\_POINT Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) that specifies where the pen flick occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6b22-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6b22-112">Remarks</span></span>

<span data-ttu-id="c6b22-113">Un gesto de lápiz es un gesto de lápiz unidireccional que requiere que el usuario se ponga en contacto con el digitalizador en un movimiento de gesto rápido y sencillo.</span><span class="sxs-lookup"><span data-stu-id="c6b22-113">A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion.</span></span> <span data-ttu-id="c6b22-114">Un gesto se caracteriza por alta velocidad y un alto grado de recta.</span><span class="sxs-lookup"><span data-stu-id="c6b22-114">A flick is characterized by high speed and a high degree of straightness.</span></span> <span data-ttu-id="c6b22-115">Un gesto se identifica por su dirección.</span><span class="sxs-lookup"><span data-stu-id="c6b22-115">A flick is identified by its direction.</span></span> <span data-ttu-id="c6b22-116">Los gestos se pueden realizar en ocho direcciones correspondientes a las direcciones de brújula cardinal y secundaria.</span><span class="sxs-lookup"><span data-stu-id="c6b22-116">Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.</span></span>

<span data-ttu-id="c6b22-117">Cuando se produce un gesto de lápiz, Windows notifica primero a una aplicación mediante el envío de un mensaje de **\_ \_ gesto de Tablet PC de WM** , que una ventana recibe a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c6b22-117">When a pen flick occurs, Windows first notifies an application by sending a **WM\_TABLET\_FLICK** message, which a window receives through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="c6b22-118">Devuelva la constante de **\_ \_ \_ máscara controlada** por el gesto de WM, descrita en el apartado de [constantes de gestos](flicks-constants.md), para indicar que la aplicación respondió al mensaje de **\_ \_ gesto de Tablet PC de WM** .</span><span class="sxs-lookup"><span data-stu-id="c6b22-118">Return the **FLICK\_WM\_HANDLED\_MASK** constant, described in [Flicks Constants](flicks-constants.md), to indicate that the application responded to the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="c6b22-119">Si la aplicación no devuelve el **gesto de la \_ \_ \_ máscara controlada de WM**, Windows realiza la acción predeterminada especificada en el panel de control de gestos mediante el envío de una notificación de seguimiento, como [**WM \_ APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM \_ VSCROLL**](../controls/wm-vscroll.md)o [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md), en función de la acción asociada con el gesto de lápiz.</span><span class="sxs-lookup"><span data-stu-id="c6b22-119">If the application does not return **FLICK\_WM\_HANDLED\_MASK**, Windows performs the default action specified in the flicks control panel by sending a follow-up notification, such as [**WM\_APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM\_VSCROLL**](../controls/wm-vscroll.md), or [**WM\_KEYDOWN**](../inputdev/wm-keydown.md), depending on which action is associated with the pen flick.</span></span>

<span data-ttu-id="c6b22-120">Tenga precaución al controlar el mensaje de **\_ \_ gestos de Tablet PC de WM** .</span><span class="sxs-lookup"><span data-stu-id="c6b22-120">Use caution when handling the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="c6b22-121">**WM \_ El \_ gesto de TABLET PC** se pasa a través de la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="c6b22-121">**WM\_TABLET\_FLICK** is passed via the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="c6b22-122">Si llama a métodos en una interfaz COM, ese objeto debe estar dentro del mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="c6b22-122">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="c6b22-123">De lo contrario, COM produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="c6b22-123">If not, COM throws an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b22-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6b22-124">Requirements</span></span>



| <span data-ttu-id="c6b22-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b22-125">Requirement</span></span> | <span data-ttu-id="c6b22-126">Value</span><span class="sxs-lookup"><span data-stu-id="c6b22-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b22-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6b22-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b22-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6b22-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c6b22-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6b22-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b22-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6b22-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c6b22-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6b22-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b22-132"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b22-132"><dt>Tpcshrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6b22-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6b22-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b22-134">**estructura de los datos de gestos \_**</span><span class="sxs-lookup"><span data-stu-id="c6b22-134">**flick\_data structure**</span></span>](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[<span data-ttu-id="c6b22-135">**\_mensaje de gesto de Tablet PC de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c6b22-135">**wm\_tablet\_flick message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="c6b22-136">gestos de gestos</span><span class="sxs-lookup"><span data-stu-id="c6b22-136">flicks gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="c6b22-137">[responder a gestos de lápiz](/previous-versions/windows/desktop/ms703447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6b22-137">[responding to pen flicks](/previous-versions/windows/desktop/ms703447(v=vs.85))</span></span>
</dt> </dl>

 

 
