---
title: Código de notificación de PGN_CALCSIZE (commctrl. h)
description: Lo envía un control de paginación para obtener las dimensiones desplazables de la ventana contenida.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802065"
---
# <a name="pgn_calcsize-notification-code"></a><span data-ttu-id="b0b3e-104">Código de notificación de CALCSIZE de PGN \_</span><span class="sxs-lookup"><span data-stu-id="b0b3e-104">PGN\_CALCSIZE notification code</span></span>

<span data-ttu-id="b0b3e-105">Lo envía un control de paginación para obtener las dimensiones desplazables de la ventana contenida.</span><span class="sxs-lookup"><span data-stu-id="b0b3e-105">Sent by a pager control to obtain the scrollable dimensions of the contained window.</span></span> <span data-ttu-id="b0b3e-106">El control de paginación utiliza estas dimensiones para determinar el tamaño desplazable de la ventana contenida.</span><span class="sxs-lookup"><span data-stu-id="b0b3e-106">These dimensions are used by the pager control to determine the scrollable size of the contained window.</span></span> <span data-ttu-id="b0b3e-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b3e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b0b3e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0b3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b3e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0b3e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b3e-110">Puntero a una estructura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que contiene y recibe información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="b0b3e-110">Pointer to an [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="b0b3e-111">El miembro **dwFlag** de esta estructura indica qué dimensión se está calculando.</span><span class="sxs-lookup"><span data-stu-id="b0b3e-111">The **dwFlag** member of this structure indicates which dimension is being calculated.</span></span> <span data-ttu-id="b0b3e-112">Dependiendo del valor de **dwFlag**, debe colocar la dimensión deseada en el miembro **iWidth** o **iHeight** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="b0b3e-112">Depending on the value of **dwFlag**, you should place the desired dimension in the **iWidth** or **iHeight** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b3e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0b3e-113">Return value</span></span>

<span data-ttu-id="b0b3e-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="b0b3e-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b3e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b3e-115">Requirements</span></span>



| <span data-ttu-id="b0b3e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b3e-116">Requirement</span></span> | <span data-ttu-id="b0b3e-117">Value</span><span class="sxs-lookup"><span data-stu-id="b0b3e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b3e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0b3e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b3e-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0b3e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0b3e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0b3e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b3e-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0b3e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0b3e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0b3e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b3e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b3e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





