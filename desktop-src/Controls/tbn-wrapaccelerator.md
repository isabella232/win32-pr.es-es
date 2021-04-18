---
title: Código de notificación de TBN_WRAPACCELERATOR (commctrl. h)
description: Solicita el índice del botón en una o más barras de herramientas correspondientes al carácter de aceleración especificado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656486"
---
# <a name="tbn_wrapaccelerator-notification-code"></a><span data-ttu-id="7ad7b-105">Código de notificación de WRAPACCELERATOR de TBN \_</span><span class="sxs-lookup"><span data-stu-id="7ad7b-105">TBN\_WRAPACCELERATOR notification code</span></span>

<span data-ttu-id="7ad7b-106">Solicita el índice del botón en una o más barras de herramientas correspondientes al carácter de aceleración especificado.</span><span class="sxs-lookup"><span data-stu-id="7ad7b-106">Requests the index of the button in one or more toolbars corresponding to the specified accelerator character.</span></span> <span data-ttu-id="7ad7b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7ad7b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7ad7b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ad7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ad7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ad7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad7b-110">Puntero a una estructura que contiene el carácter de tecla de aceleración y que recibe el índice del botón correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7ad7b-110">A pointer to a structure that contains the accelerator key character, and that receives the index of the corresponding button.</span></span> <span data-ttu-id="7ad7b-111">El índice es-1 si el acelerador no se corresponde con un comando.</span><span class="sxs-lookup"><span data-stu-id="7ad7b-111">The index is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ad7b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ad7b-112">Return value</span></span>

<span data-ttu-id="7ad7b-113">**True** si se devuelve un índice; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7ad7b-113">**TRUE** if an index is returned, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ad7b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ad7b-114">Remarks</span></span>

<span data-ttu-id="7ad7b-115">Es posible que las aplicaciones con una o más barras de herramientas reciban este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7ad7b-115">Applications with one or more toolbars may receive this notification code.</span></span>

<span data-ttu-id="7ad7b-116">La estructura **NMTBWRAPACCELERATOR** debe definirse mediante la aplicación de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7ad7b-116">The **NMTBWRAPACCELERATOR** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="7ad7b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ad7b-117">Requirements</span></span>



| <span data-ttu-id="7ad7b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ad7b-118">Requirement</span></span> | <span data-ttu-id="7ad7b-119">Value</span><span class="sxs-lookup"><span data-stu-id="7ad7b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad7b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ad7b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7ad7b-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7ad7b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ad7b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ad7b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7ad7b-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ad7b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ad7b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ad7b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ad7b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad7b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





