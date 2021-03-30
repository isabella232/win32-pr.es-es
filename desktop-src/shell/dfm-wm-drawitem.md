---
description: Se envía a la ventana primaria de un control o menú dibujado por el propietario cuando ha cambiado un aspecto visual del control o menú.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Mensaje de DFM_WM_DRAWITEM (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984294"
---
# <a name="dfm_wm_drawitem-message"></a><span data-ttu-id="39359-103">Mensaje de DFM \_ WM \_ DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="39359-103">DFM\_WM\_DRAWITEM message</span></span>

<span data-ttu-id="39359-104">Se envía a la ventana primaria de un control o menú dibujado por el propietario cuando ha cambiado un aspecto visual del control o menú.</span><span class="sxs-lookup"><span data-stu-id="39359-104">Sent to the parent window of an owner-drawn control or menu when a visual aspect of the control or menu has changed.</span></span>


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a><span data-ttu-id="39359-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39359-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39359-106">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39359-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39359-107">Identificador del control que envió el mensaje de **DFM \_ WM \_ DRAWITEM** .</span><span class="sxs-lookup"><span data-stu-id="39359-107">The identifier of the control that sent the **DFM\_WM\_DRAWITEM** message.</span></span> <span data-ttu-id="39359-108">Si el mensaje se envió mediante un menú, este parámetro es cero.</span><span class="sxs-lookup"><span data-stu-id="39359-108">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="39359-109">*lpDrawItem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39359-109">*lpDrawItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39359-110">Puntero a una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene información sobre el elemento que se va a dibujar y el tipo de dibujo necesario.</span><span class="sxs-lookup"><span data-stu-id="39359-110">A pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39359-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39359-111">Return value</span></span>

<span data-ttu-id="39359-112">Si una aplicación procesa este mensaje, debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="39359-112">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="39359-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39359-113">Remarks</span></span>

<span data-ttu-id="39359-114">El miembro **del itemaction** de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica la operación de dibujo que una aplicación debe realizar.</span><span class="sxs-lookup"><span data-stu-id="39359-114">The **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="39359-115">Antes de volver a procesar este mensaje, una aplicación debe asegurarse de que el contexto de dispositivo identificado por el miembro **HDC** de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) está en el estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="39359-115">Before returning from processing this message, an application should ensure that the device context identified by the **hDC** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="39359-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39359-116">Requirements</span></span>



| <span data-ttu-id="39359-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="39359-117">Requirement</span></span> | <span data-ttu-id="39359-118">Value</span><span class="sxs-lookup"><span data-stu-id="39359-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39359-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39359-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39359-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="39359-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="39359-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39359-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39359-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="39359-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39359-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39359-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39359-124"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="39359-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
