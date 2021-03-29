---
title: Mensaje de HDN_ITEMSTATEICONCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el icono de estado de un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- HDN_ITEMSTATEICONCLICK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493054"
---
# <a name="hdn_itemstateiconclick-message"></a><span data-ttu-id="709d0-105">HDN \_ ITEMSTATEICONCLICK</span><span class="sxs-lookup"><span data-stu-id="709d0-105">HDN\_ITEMSTATEICONCLICK message</span></span>

<span data-ttu-id="709d0-106">Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el icono de estado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="709d0-106">Notifies a header control's parent window that the user clicked an item's state icon.</span></span> <span data-ttu-id="709d0-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="709d0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="709d0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="709d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="709d0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="709d0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="709d0-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información adicional sobre el icono de estado en el que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="709d0-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the state icon that was clicked on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="709d0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="709d0-111">Return value</span></span>

<span data-ttu-id="709d0-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="709d0-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="709d0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="709d0-113">Requirements</span></span>



| <span data-ttu-id="709d0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="709d0-114">Requirement</span></span> | <span data-ttu-id="709d0-115">Value</span><span class="sxs-lookup"><span data-stu-id="709d0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="709d0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="709d0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="709d0-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="709d0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="709d0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="709d0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="709d0-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="709d0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="709d0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="709d0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="709d0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="709d0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





