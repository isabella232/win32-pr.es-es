---
title: Código de notificación de NM_NCHITTEST (rebar) (commctrl. h)
description: Lo envía un control Rebar cuando el control recibe un mensaje de NCHITTEST de WM \_ . Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Código de notificación NM_NCHITTEST (rebar) controles de Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150758"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="28ce6-105">Código de notificación de NM \_ NCHITTEST (rebar)</span><span class="sxs-lookup"><span data-stu-id="28ce6-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="28ce6-106">Lo envía un control Rebar cuando el control recibe un mensaje de [**\_ NCHITTEST de WM**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="28ce6-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="28ce6-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="28ce6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="28ce6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28ce6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ce6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28ce6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28ce6-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="28ce6-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="28ce6-111">El miembro **dwItemSpec** contiene el índice de banda sobre el que se produjo el mensaje de la prueba de posicionamiento y el miembro **PT** contiene las coordenadas del mouse del mensaje de la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="28ce6-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ce6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28ce6-112">Return value</span></span>

<span data-ttu-id="28ce6-113">Devuelva cero para permitir que el rebar realice el procesamiento predeterminado del mensaje de la prueba de posicionamiento, o bien devuelva uno de los valores de HT \* documentados en [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para invalidar el procesamiento predeterminado de la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="28ce6-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ce6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28ce6-114">Requirements</span></span>



| <span data-ttu-id="28ce6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="28ce6-115">Requirement</span></span> | <span data-ttu-id="28ce6-116">Value</span><span class="sxs-lookup"><span data-stu-id="28ce6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28ce6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28ce6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28ce6-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="28ce6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28ce6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28ce6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="28ce6-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="28ce6-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28ce6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28ce6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="28ce6-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ce6-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

