---
title: Mensaje de TTM_SETTOOLINFO (commctrl. h)
description: Establece la información que mantiene un control ToolTip para una herramienta.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- TTM_SETTOOLINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492844"
---
# <a name="ttm_settoolinfo-message"></a><span data-ttu-id="020ee-104">TTM \_ SETTOOLINFO</span><span class="sxs-lookup"><span data-stu-id="020ee-104">TTM\_SETTOOLINFO message</span></span>

<span data-ttu-id="020ee-105">Establece la información que mantiene un control ToolTip para una herramienta.</span><span class="sxs-lookup"><span data-stu-id="020ee-105">Sets the information that a tooltip control maintains for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="020ee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="020ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="020ee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="020ee-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="020ee-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="020ee-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="020ee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="020ee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="020ee-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que especifica la información que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="020ee-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that specifies the information to set.</span></span> <span data-ttu-id="020ee-111">El miembro **cbSize** de esta estructura debe establecerse antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="020ee-111">The **cbSize** member of this structure must be set before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="020ee-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="020ee-112">Return value</span></span>

<span data-ttu-id="020ee-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="020ee-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="020ee-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="020ee-114">Remarks</span></span>

<span data-ttu-id="020ee-115">Algunas propiedades internas de una herramienta se establecen cuando se crea la herramienta y no se vuelven a calcular cuando se envía un mensaje **\_ SETTOOLINFO de TTM** .</span><span class="sxs-lookup"><span data-stu-id="020ee-115">Some internal properties of a tool are established when the tool is created, and are not recomputed when a **TTM\_SETTOOLINFO** message is sent.</span></span> <span data-ttu-id="020ee-116">Si simplemente asigna valores a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) y lo pasa al control ToolTip con un mensaje **TTM \_ SETTOOLINFO** , estas propiedades se pueden perder.</span><span class="sxs-lookup"><span data-stu-id="020ee-116">If you simply assign values to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure and pass it to the tooltip control with a **TTM\_SETTOOLINFO** message, these properties may be lost.</span></span> <span data-ttu-id="020ee-117">En su lugar, la aplicación debe solicitar primero la estructura **TOOLINFO** actual de la herramienta mediante el envío del mensaje de control de información sobre herramientas [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="020ee-117">Instead, your application should first request the tool's current **TOOLINFO** structure by sending the tooltip control a [**TTM\_GETTOOLINFO**](ttm-gettoolinfo.md) message.</span></span> <span data-ttu-id="020ee-118">A continuación, modifique los miembros de esta estructura según sea necesario y páselo de vuelta al control ToolTip con **TTM \_ SETTOOLINFO**.</span><span class="sxs-lookup"><span data-stu-id="020ee-118">Then, modify the members of this structure as needed and pass it back to the tooltip control with **TTM\_SETTOOLINFO**.</span></span>

<span data-ttu-id="020ee-119">Al llamar a **TTM \_ SETTOOLINFO**, la cadena a la que apunta el miembro **LpszText** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) no debe superar los 80 **TCHARs** de longitud, incluido el **valor null** final.</span><span class="sxs-lookup"><span data-stu-id="020ee-119">When calling **TTM\_SETTOOLINFO**, the string pointed to by the **lpszText** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure must not exceed 80 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="020ee-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="020ee-120">Requirements</span></span>



| <span data-ttu-id="020ee-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="020ee-121">Requirement</span></span> | <span data-ttu-id="020ee-122">Value</span><span class="sxs-lookup"><span data-stu-id="020ee-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="020ee-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="020ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="020ee-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="020ee-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="020ee-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="020ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="020ee-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="020ee-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="020ee-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="020ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="020ee-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="020ee-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="020ee-129">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="020ee-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="020ee-130">**TTM \_ SETTOOLINFOW** (Unicode) y **TTM \_ SETTOOLINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="020ee-130">**TTM\_SETTOOLINFOW** (Unicode) and **TTM\_SETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





