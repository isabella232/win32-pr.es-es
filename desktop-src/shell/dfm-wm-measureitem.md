---
description: Se envía a la ventana propietaria de un control o un elemento de menú cuando se crea el control o el menú.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Mensaje de DFM_WM_MEASUREITEM (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423704"
---
# <a name="dfm_wm_measureitem-message"></a><span data-ttu-id="8f72c-103">DFM \_ WM \_ MEASUREITEM Message</span><span class="sxs-lookup"><span data-stu-id="8f72c-103">DFM\_WM\_MEASUREITEM message</span></span>

<span data-ttu-id="8f72c-104">Se envía a la ventana propietaria de un control o un elemento de menú cuando se crea el control o el menú.</span><span class="sxs-lookup"><span data-stu-id="8f72c-104">Sent to the owner window of a control or menu item when the control or menu is created.</span></span>


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a><span data-ttu-id="8f72c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f72c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f72c-106">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f72c-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f72c-107">El valor del miembro **CtlID** de la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) señalada por el parámetro *lpMeasureItem* .</span><span class="sxs-lookup"><span data-stu-id="8f72c-107">The value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter.</span></span> <span data-ttu-id="8f72c-108">Este valor identifica el control que envió el mensaje **DFM de \_ \_ MEASUREITEM de WM** .</span><span class="sxs-lookup"><span data-stu-id="8f72c-108">This value identifies the control that sent the **DFM\_WM\_MEASUREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="8f72c-109">*lpMeasureItem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f72c-109">*lpMeasureItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f72c-110">Puntero a una estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contiene las dimensiones del elemento de menú o control dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="8f72c-110">A pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f72c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f72c-111">Remarks</span></span>

<span data-ttu-id="8f72c-112">Cuando la ventana propietaria recibe el mensaje **DFM de \_ \_ MEASUREITEM WM** , el propietario rellena la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) señalada por el parámetro *lpMeasureItem* del mensaje y devuelve; esto informa al sistema de las dimensiones del control.</span><span class="sxs-lookup"><span data-stu-id="8f72c-112">When the owner window receives the **DFM\_WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f72c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f72c-113">Requirements</span></span>



| <span data-ttu-id="8f72c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f72c-114">Requirement</span></span> | <span data-ttu-id="8f72c-115">Value</span><span class="sxs-lookup"><span data-stu-id="8f72c-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f72c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f72c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8f72c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8f72c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8f72c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f72c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8f72c-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f72c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8f72c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f72c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f72c-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f72c-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
