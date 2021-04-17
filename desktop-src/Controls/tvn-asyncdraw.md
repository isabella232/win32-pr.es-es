---
title: Código de notificación de TVN_ASYNCDRAW (commctrl. h)
description: Lo envía un control de vista de árbol a su elemento primario cuando se produce un error en el dibujo de un icono o una superposición. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658365"
---
# <a name="tvn_asyncdraw-notification-code"></a><span data-ttu-id="202fb-105">Código de notificación de ASYNCDRAW de TVN \_</span><span class="sxs-lookup"><span data-stu-id="202fb-105">TVN\_ASYNCDRAW notification code</span></span>

<span data-ttu-id="202fb-106">Lo envía un control de vista de árbol a su elemento primario cuando se produce un error en el dibujo de un icono o una superposición.</span><span class="sxs-lookup"><span data-stu-id="202fb-106">Sent by a tree-view control to its parent when the drawing of a icon or overlay has failed.</span></span> <span data-ttu-id="202fb-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="202fb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="202fb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="202fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="202fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="202fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="202fb-110">Puntero a una estructura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="202fb-110">Pointer to an [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="202fb-111">La estructura **NMTVASYNCDRAW** contiene la razón por la que se produjo un error en Draw.</span><span class="sxs-lookup"><span data-stu-id="202fb-111">The **NMTVASYNCDRAW** structure contains the reason the draw failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="202fb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="202fb-112">Return value</span></span>

<span data-ttu-id="202fb-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="202fb-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="202fb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="202fb-114">Remarks</span></span>

<span data-ttu-id="202fb-115">El control de vista de árbol debe tener el estilo extendido [**TV \_ ex \_ DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="202fb-115">The tree-view control must have the [**TVS\_EX\_DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="202fb-116">Tenga en cuenta que esto es equivalente a la marca de LVN ASYNCDRAWN de la vista de lista \_ y su estilo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="202fb-116">Note that this is equivalent to list-view's LVN\_ASYNCDRAWN flag and its corresponding style.</span></span>

<span data-ttu-id="202fb-117">Este control no se dibuja de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="202fb-117">This control does not draw asynchronously.</span></span> <span data-ttu-id="202fb-118">Asincrónico se utiliza en el contexto de que el control de vista de árbol no extraiga una imagen de forma sincrónica si no está disponible.</span><span class="sxs-lookup"><span data-stu-id="202fb-118">Asynchronous is used in the context that the tree-view control does not synchronously extract an image if it is not available.</span></span> <span data-ttu-id="202fb-119">(Por ejemplo, es posible que la imagen no esté disponible si el control de vista de árbol usa una lista de imágenes dispersas, ya que se puede descargar la imagen). En su lugar, cuando una imagen no está disponible, el control pide sincrónicamente al elemento primario qué acción debe realizar mediante el envío de una notificación primaria a TVN \_ ASYNCDRAW con una estructura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="202fb-119">(For instance, the image may not be available if the tree-view control uses a sparse image list, since the image may be unloaded.) Instead, when an image is not available, the control synchronously asks the parent what action to take by sending the parent an TVN\_ASYNCDRAW notification with a [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="202fb-120">El miembro **HR** de esta estructura describe la razón por la que se produjo un error en la traza del control.</span><span class="sxs-lookup"><span data-stu-id="202fb-120">The **hr** member of this structure describes the reason the control's draw failed.</span></span> <span data-ttu-id="202fb-121">Un resultado de **HR** de E \_ Pending significa que la imagen no está presente en absoluto (es necesario extraer la imagen).</span><span class="sxs-lookup"><span data-stu-id="202fb-121">An **hr** result of E\_PENDING means the image is not present at all (the image needs to be extracted).</span></span> <span data-ttu-id="202fb-122">Success indica que la imagen está presente pero no con la calidad de imagen requerida.</span><span class="sxs-lookup"><span data-stu-id="202fb-122">Success indicates that the image is present but not at the required image quality.</span></span>

<span data-ttu-id="202fb-123">El elemento primario establece el miembro **dwRetFlags** de la estructura para informar al control de cómo continuar.</span><span class="sxs-lookup"><span data-stu-id="202fb-123">The parent sets the **dwRetFlags** member of the structure to inform the control how to proceed.</span></span> <span data-ttu-id="202fb-124">Por ejemplo, el elemento primario puede devolver otra imagen, en el miembro **iRetImageIndex** , para que el control dibuje.</span><span class="sxs-lookup"><span data-stu-id="202fb-124">For instance, the parent may return another image, in the **iRetImageIndex** member, for the control to draw.</span></span> <span data-ttu-id="202fb-125">En este caso, el elemento primario establece el miembro **dwRetFlags** en ADRF \_ DRAWIMAGE.</span><span class="sxs-lookup"><span data-stu-id="202fb-125">In this case, the parent sets the **dwRetFlags** member to ADRF\_DRAWIMAGE.</span></span> <span data-ttu-id="202fb-126">Si el control encuentra la imagen devuelta no se ha extraído, \_ puede que el control envíe otra notificación TVN ASYNCDRAW.</span><span class="sxs-lookup"><span data-stu-id="202fb-126">If the control finds the returned image has not been extracted, yet another TVN\_ASYNCDRAW notification may be sent by the control.</span></span>

<span data-ttu-id="202fb-127">Si una imagen no está disponible, la idea detrás de asincrónica es permitir que el elemento primario realice la extracción en segundo plano para que la extracción no bloquee el subproceso de la interfaz de usuario, es decir, el subproceso en el que se encuentra el control.</span><span class="sxs-lookup"><span data-stu-id="202fb-127">If an image is not available, the idea behind asynchronous is to allow the parent do the extraction in the background so that extraction does not block the UI thread, that is, the thread the control is on.</span></span> <span data-ttu-id="202fb-128">El elemento primario puede devolver ADRF \_ DRAWNOTHING al control y, a continuación, iniciar un subproceso en segundo plano para extraer el icono.</span><span class="sxs-lookup"><span data-stu-id="202fb-128">The parent may return ADRF\_DRAWNOTHING to the control, then launch a background thread to extract the icon.</span></span> <span data-ttu-id="202fb-129">Una vez extraído, el elemento primario puede establecer el icono en el control TreeView con la macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span><span class="sxs-lookup"><span data-stu-id="202fb-129">Once extracted, the parent may set the icon in the treeview control with macro [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span></span> <span data-ttu-id="202fb-130">Esto hace que la vista de árbol invalide el elemento y, finalmente, lo vuelva a dibujar con la imagen extraída en la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="202fb-130">This causes tree-view to invalidate the item and eventually repaint it with the extracted image in the image list.</span></span>

<span data-ttu-id="202fb-131">En el ejemplo de código siguiente, que se va a usar como parte de un programa más grande, se muestra cómo un control primario puede procesar dos posibles códigos de retorno en esta notificación por un control y decidir qué acción debe realizar el control.</span><span class="sxs-lookup"><span data-stu-id="202fb-131">The following code example, to be used as part of a larger program, shows how a parent may process two possible return codes in this notification by a control, and decide what action the control should take.</span></span> <span data-ttu-id="202fb-132">No se muestra el valor de **dwRetFlags** .</span><span class="sxs-lookup"><span data-stu-id="202fb-132">Setting **dwRetFlags** is not shown.</span></span>


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a><span data-ttu-id="202fb-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="202fb-133">Requirements</span></span>



| <span data-ttu-id="202fb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="202fb-134">Requirement</span></span> | <span data-ttu-id="202fb-135">Value</span><span class="sxs-lookup"><span data-stu-id="202fb-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="202fb-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="202fb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="202fb-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="202fb-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="202fb-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="202fb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="202fb-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="202fb-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="202fb-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="202fb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="202fb-141"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="202fb-141"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





