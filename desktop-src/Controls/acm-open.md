---
title: Mensaje de ACM_OPEN (commctrl. h)
description: Abre un clip AVI y muestra su primer fotograma en un control Animation. Puede enviar este mensaje explícitamente o utilizar la macro de animación \_ Open o Animate \_ OpenEx. Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422049"
---
# <a name="acm_open-message"></a><span data-ttu-id="19ce6-106">\_Mensaje abierto de ACM</span><span class="sxs-lookup"><span data-stu-id="19ce6-106">ACM\_OPEN message</span></span>

<span data-ttu-id="19ce6-107">Abre un clip AVI y muestra su primer fotograma en un control Animation.</span><span class="sxs-lookup"><span data-stu-id="19ce6-107">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="19ce6-108">Puede enviar este mensaje explícitamente o utilizar la macro de [**animación \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) o [**Animate \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) .</span><span class="sxs-lookup"><span data-stu-id="19ce6-108">You can send this message explicitly or use the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) or [**Animate\_OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) macro.</span></span> <span data-ttu-id="19ce6-109">Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.</span><span class="sxs-lookup"><span data-stu-id="19ce6-109">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

## <a name="parameters"></a><span data-ttu-id="19ce6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19ce6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ce6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19ce6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19ce6-112">[Versión 4,71](common-control-versions.md) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="19ce6-112">[Version 4.71](common-control-versions.md) and later.</span></span> <span data-ttu-id="19ce6-113">Identificador de instancia del módulo del que se debe cargar el recurso.</span><span class="sxs-lookup"><span data-stu-id="19ce6-113">An instance handle to the module from which the resource should be loaded.</span></span> <span data-ttu-id="19ce6-114">Establezca este valor en **null** para que el control use el valor de hInstance que se usa para crear la ventana.</span><span class="sxs-lookup"><span data-stu-id="19ce6-114">Set this value to **NULL** to have the control use the HINSTANCE value used to create the window.</span></span> <span data-ttu-id="19ce6-115">Tenga en cuenta que si una DLL crea la ventana, el valor predeterminado de *wParam* es el valor de hInstance del archivo dll, no de la aplicación que llama al archivo dll.</span><span class="sxs-lookup"><span data-stu-id="19ce6-115">Note that if the window is created by a DLL, the default value for *wParam* is the HINSTANCE value of the DLL, not of the application that calls the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="19ce6-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19ce6-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19ce6-117">Un puntero a un búfer que contiene la ruta de acceso del archivo AVI o el nombre de un recurso AVI.</span><span class="sxs-lookup"><span data-stu-id="19ce6-117">A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource.</span></span> <span data-ttu-id="19ce6-118">Como alternativa, este parámetro puede constar del identificador de recursos AVI en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y cero en [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19ce6-118">Alternatively, this parameter can consist of the AVI resource identifier in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and zero in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="19ce6-119">Para crear este valor, use la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="19ce6-119">To create this value, use the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="19ce6-120">El control carga el recurso AVI desde el módulo especificado por el identificador de instancia que se ha pasado a la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , a la [**animación de \_ creación**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) de macros o a la función de creación de cuadros de diálogo que creó el control.</span><span class="sxs-lookup"><span data-stu-id="19ce6-120">The control loads the AVI resource from the module specified by the instance handle passed to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function, the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro, or the dialog box creation function that created the control.</span></span> <span data-ttu-id="19ce6-121">En la [versión 4,71](common-control-versions.md) y posteriores, el recurso se carga desde el módulo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="19ce6-121">In [Version 4.71](common-control-versions.md) and later, the resource is loaded from the module specified by *wParam*.</span></span> <span data-ttu-id="19ce6-122">Un recurso AVI debe tener el tipo "AVI".</span><span class="sxs-lookup"><span data-stu-id="19ce6-122">An AVI resource must have the "AVI" type.</span></span> <span data-ttu-id="19ce6-123">Si este parámetro es **null**, el sistema cierra el archivo AVI que se abrió previamente para el control de animación especificado, si existe.</span><span class="sxs-lookup"><span data-stu-id="19ce6-123">If this parameter is **NULL**, the system closes the AVI file that was previously opened for the specified animation control, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ce6-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19ce6-124">Return value</span></span>

<span data-ttu-id="19ce6-125">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="19ce6-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="19ce6-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19ce6-126">Remarks</span></span>

<span data-ttu-id="19ce6-127">El archivo AVI o el recurso especificado por *lpszName* no debe contener audio.</span><span class="sxs-lookup"><span data-stu-id="19ce6-127">The AVI file or resource specified by *lpszName* must not contain audio.</span></span>

<span data-ttu-id="19ce6-128">Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.</span><span class="sxs-lookup"><span data-stu-id="19ce6-128">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

<span data-ttu-id="19ce6-129">Solo puede abrir clips AVI silenciosos.</span><span class="sxs-lookup"><span data-stu-id="19ce6-129">You can only open silent AVI clips.</span></span> <span data-ttu-id="19ce6-130">ACM \_ Open and [**Animate \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) FAIL si *lParam* especifica un clip AVI que contiene sonido.</span><span class="sxs-lookup"><span data-stu-id="19ce6-130">ACM\_OPEN and [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) fail if *lParam* specifies an AVI clip that contains sound.</span></span>

<span data-ttu-id="19ce6-131">Puede usar [**animar \_ cerrar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) para cerrar un archivo AVI o un recurso AVI que se abrió previamente para el control de animación especificado.</span><span class="sxs-lookup"><span data-stu-id="19ce6-131">You can use [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) to close an AVI file or AVI resource that was previously opened for the specified animation control.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ce6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19ce6-132">Requirements</span></span>



| <span data-ttu-id="19ce6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ce6-133">Requirement</span></span> | <span data-ttu-id="19ce6-134">Value</span><span class="sxs-lookup"><span data-stu-id="19ce6-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19ce6-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19ce6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="19ce6-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19ce6-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19ce6-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19ce6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="19ce6-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="19ce6-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19ce6-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19ce6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="19ce6-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ce6-140"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="19ce6-141">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="19ce6-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="19ce6-142">**ACM \_ OPENW** (Unicode) y **ACM \_ opena** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="19ce6-142">**ACM\_OPENW** (Unicode) and **ACM\_OPENA** (ANSI)</span></span><br/>                         |



 

