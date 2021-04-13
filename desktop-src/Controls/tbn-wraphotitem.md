---
title: Código de notificación de TBN_WRAPHOTITEM (commctrl. h)
description: Notifica a una aplicación con dos o más barras de herramientas que el elemento activo va a cambiar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490192"
---
# <a name="tbn_wraphotitem-notification-code"></a><span data-ttu-id="fefe1-105">Código de notificación de WRAPHOTITEM de TBN \_</span><span class="sxs-lookup"><span data-stu-id="fefe1-105">TBN\_WRAPHOTITEM notification code</span></span>

<span data-ttu-id="fefe1-106">Notifica a una aplicación con dos o más barras de herramientas que el elemento activo va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="fefe1-106">Notifies an application with two or more toolbars that the hot item is about to change.</span></span> <span data-ttu-id="fefe1-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fefe1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fefe1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fefe1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fefe1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fefe1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fefe1-110">Puntero a una estructura que contiene el elemento activo anterior (**iStart**) y si el nuevo elemento activo está delante de él (**iDir** =-1) o después de él (**iDir** = 1), así como un motivo por el que el elemento activo está cambiando.</span><span class="sxs-lookup"><span data-stu-id="fefe1-110">A pointer to a structure that contains the old hot item (**iStart**) and whether the new hot item is before it (**iDir** = -1) or after it (**iDir** = 1), as well as a reason why the hot item is changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fefe1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fefe1-111">Return value</span></span>

<span data-ttu-id="fefe1-112">**True** si la aplicación controla el propio cambio de elemento activo. en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="fefe1-112">**TRUE** if the application is handling the hot item change itself; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fefe1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fefe1-113">Remarks</span></span>

<span data-ttu-id="fefe1-114">La estructura **NMTBWRAPHOTITEM** debe definirse mediante la aplicación de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fefe1-114">The **NMTBWRAPHOTITEM** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a><span data-ttu-id="fefe1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fefe1-115">Requirements</span></span>



| <span data-ttu-id="fefe1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fefe1-116">Requirement</span></span> | <span data-ttu-id="fefe1-117">Value</span><span class="sxs-lookup"><span data-stu-id="fefe1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fefe1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fefe1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fefe1-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fefe1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fefe1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fefe1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fefe1-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fefe1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fefe1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fefe1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fefe1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fefe1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





