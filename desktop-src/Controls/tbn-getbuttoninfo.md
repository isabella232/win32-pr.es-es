---
title: Código de notificación de TBN_GETBUTTONINFO (commctrl. h)
description: Recupera información de personalización de la barra de herramientas y notifica a la ventana primaria de la barra de herramientas los cambios realizados en la barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996797"
---
# <a name="tbn_getbuttoninfo-notification-code"></a><span data-ttu-id="02f5e-105">Código de notificación de GETBUTTONINFO de TBN \_</span><span class="sxs-lookup"><span data-stu-id="02f5e-105">TBN\_GETBUTTONINFO notification code</span></span>

<span data-ttu-id="02f5e-106">Recupera información de personalización de la barra de herramientas y notifica a la ventana primaria de la barra de herramientas los cambios realizados en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="02f5e-106">Retrieves toolbar customization information and notifies the toolbar's parent window of any changes being made to the toolbar.</span></span> <span data-ttu-id="02f5e-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="02f5e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="02f5e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02f5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02f5e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02f5e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02f5e-110">Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="02f5e-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="02f5e-111">El miembro **iItem** especifica un índice basado en cero que proporciona un recuento de los botones que el cuadro de diálogo Personalizar barra de herramientas muestra como disponibles y presentes en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="02f5e-111">The **iItem** member specifies a zero-based index that provides a count of the buttons the Customize Toolbar dialog box displays as both available and present on the toolbar.</span></span> <span data-ttu-id="02f5e-112">El miembro **miembros pszText** especifica la dirección del texto del botón actual y **cchText** especifica su longitud en caracteres.</span><span class="sxs-lookup"><span data-stu-id="02f5e-112">The **pszText** member specifies the address of the current button text, and **cchText** specifies its length in characters.</span></span> <span data-ttu-id="02f5e-113">La aplicación debe rellenar la estructura con información acerca del botón.</span><span class="sxs-lookup"><span data-stu-id="02f5e-113">The application should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02f5e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02f5e-114">Return value</span></span>

<span data-ttu-id="02f5e-115">Devuelve **true** si la información del botón se copió en la estructura especificada o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="02f5e-115">Returns **TRUE** if button information was copied to the specified structure, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f5e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02f5e-116">Remarks</span></span>

<span data-ttu-id="02f5e-117">El control de barra de herramientas asigna un búfer y el receptor (ventana primaria) debe copiar el texto en ese búfer.</span><span class="sxs-lookup"><span data-stu-id="02f5e-117">The toolbar control allocates a buffer, and the receiver (parent window) must copy the text into that buffer.</span></span> <span data-ttu-id="02f5e-118">El miembro **cchText** contiene la longitud del búfer asignado por la barra de herramientas cuando \_ se envía TBN GETBUTTONINFO a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="02f5e-118">The **cchText** member contains the length of the buffer allocated by the toolbar when TBN\_GETBUTTONINFO is sent to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f5e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02f5e-119">Requirements</span></span>



| <span data-ttu-id="02f5e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="02f5e-120">Requirement</span></span> | <span data-ttu-id="02f5e-121">Value</span><span class="sxs-lookup"><span data-stu-id="02f5e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02f5e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02f5e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="02f5e-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="02f5e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02f5e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02f5e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="02f5e-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="02f5e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02f5e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02f5e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="02f5e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="02f5e-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="02f5e-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="02f5e-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="02f5e-129">**TBN \_ GETBUTTONINFOW** (Unicode) y **TBN \_ GETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="02f5e-129">**TBN\_GETBUTTONINFOW** (Unicode) and **TBN\_GETBUTTONINFOA** (ANSI)</span></span><br/>       |



 

 





