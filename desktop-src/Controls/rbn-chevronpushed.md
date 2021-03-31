---
title: Código de notificación de RBN_CHEVRONPUSHED (commctrl. h)
description: Se envía por un control Rebar cuando se inserta un botón de contenido adicional. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079352"
---
# <a name="rbn_chevronpushed-notification-code"></a><span data-ttu-id="129a1-105">Código de notificación de CHEVRONPUSHED de RBN \_</span><span class="sxs-lookup"><span data-stu-id="129a1-105">RBN\_CHEVRONPUSHED notification code</span></span>

<span data-ttu-id="129a1-106">Se envía por un control Rebar cuando se inserta un botón de contenido adicional.</span><span class="sxs-lookup"><span data-stu-id="129a1-106">Sent by a rebar control when a chevron is pushed.</span></span> <span data-ttu-id="129a1-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="129a1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a><span data-ttu-id="129a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="129a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="129a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="129a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="129a1-110">Puntero a la estructura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) de la banda.</span><span class="sxs-lookup"><span data-stu-id="129a1-110">Pointer to the band's [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="129a1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="129a1-111">Return value</span></span>

<span data-ttu-id="129a1-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="129a1-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="129a1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="129a1-113">Remarks</span></span>

<span data-ttu-id="129a1-114">Cuando una aplicación recibe este código de notificación, es responsable de mostrar un menú emergente con elementos para cada herramienta oculta.</span><span class="sxs-lookup"><span data-stu-id="129a1-114">When an application receives this notification code, it is responsible for displaying a popup menu with items for each hidden tool.</span></span> <span data-ttu-id="129a1-115">Use el miembro **RC** de la estructura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) para buscar la posición correcta del menú emergente.</span><span class="sxs-lookup"><span data-stu-id="129a1-115">Use the **rc** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure to find the correct position for the popup menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="129a1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="129a1-116">Requirements</span></span>



| <span data-ttu-id="129a1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="129a1-117">Requirement</span></span> | <span data-ttu-id="129a1-118">Value</span><span class="sxs-lookup"><span data-stu-id="129a1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="129a1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="129a1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="129a1-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="129a1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="129a1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="129a1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="129a1-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="129a1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="129a1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="129a1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="129a1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="129a1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





