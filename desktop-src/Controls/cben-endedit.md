---
title: Código de notificación de CBEN_ENDEDIT (commctrl. h)
description: Se envía cuando el usuario ha finalizado una operación en el cuadro de edición o ha seleccionado un elemento de la lista desplegable del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421951"
---
# <a name="cben_endedit-notification-code"></a><span data-ttu-id="a82e6-105">Código de notificación de CBEN \_ ENDEDIT</span><span class="sxs-lookup"><span data-stu-id="a82e6-105">CBEN\_ENDEDIT notification code</span></span>

<span data-ttu-id="a82e6-106">Se envía cuando el usuario ha finalizado una operación en el cuadro de edición o ha seleccionado un elemento de la lista desplegable del control.</span><span class="sxs-lookup"><span data-stu-id="a82e6-106">Sent when the user has concluded an operation within the edit box or has selected an item from the control's drop-down list.</span></span> <span data-ttu-id="a82e6-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a82e6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a82e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a82e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a82e6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a82e6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a82e6-110">Puntero a una estructura [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) que contiene información sobre cómo el usuario ha concluido la operación de edición.</span><span class="sxs-lookup"><span data-stu-id="a82e6-110">A pointer to an [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) structure that contains information about how the user concluded the edit operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a82e6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a82e6-111">Return value</span></span>

<span data-ttu-id="a82e6-112">**False** para aceptar el código de notificación y permitir que el control muestre el elemento seleccionado; en caso contrario, **true**.</span><span class="sxs-lookup"><span data-stu-id="a82e6-112">**FALSE** to accept the notification code and allow the control to display the selected item; otherwise, **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a82e6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a82e6-113">Requirements</span></span>



| <span data-ttu-id="a82e6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a82e6-114">Requirement</span></span> | <span data-ttu-id="a82e6-115">Value</span><span class="sxs-lookup"><span data-stu-id="a82e6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a82e6-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a82e6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a82e6-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a82e6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a82e6-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a82e6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a82e6-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a82e6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a82e6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a82e6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a82e6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a82e6-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a82e6-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a82e6-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a82e6-123">**CBEN \_ ENDEDITW** (Unicode) y **CBEN \_ ENDEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a82e6-123">**CBEN\_ENDEDITW** (Unicode) and **CBEN\_ENDEDITA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a82e6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a82e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82e6-125">Acerca de los controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="a82e6-125">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> </dl>

 

 





