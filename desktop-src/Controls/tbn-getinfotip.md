---
title: Código de notificación de TBN_GETINFOTIP (commctrl. h)
description: Recupera información de recuadro informativo para un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079117"
---
# <a name="tbn_getinfotip-notification-code"></a><span data-ttu-id="5471d-105">Código de notificación de GETINFOTIP de TBN \_</span><span class="sxs-lookup"><span data-stu-id="5471d-105">TBN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="5471d-106">Recupera información de recuadro informativo para un elemento de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="5471d-106">Retrieves infotip information for a toolbar item.</span></span> <span data-ttu-id="5471d-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5471d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5471d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5471d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5471d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5471d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5471d-110">Puntero a una estructura [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) que contiene información sobre los elementos y recibe información de recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="5471d-110">Pointer to an [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) structure that contains item information and receives infotip information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5471d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5471d-111">Return value</span></span>

<span data-ttu-id="5471d-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="5471d-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="5471d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5471d-113">Remarks</span></span>

<span data-ttu-id="5471d-114">La compatibilidad con el recuadro informativo de la barra de herramientas permite que la barra de herramientas muestre información sobre herramientas para los elementos que tienen un tamaño de INFOTIPSIZE caracteres.</span><span class="sxs-lookup"><span data-stu-id="5471d-114">The infotip support in the toolbar allows the toolbar to display tooltips for items that are as large as INFOTIPSIZE characters.</span></span> <span data-ttu-id="5471d-115">Si no se procesa este código de notificación, la barra de herramientas usará el texto del elemento para el recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="5471d-115">If this notification code is not processed, the toolbar will use the item's text for the infotip.</span></span>

## <a name="requirements"></a><span data-ttu-id="5471d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5471d-116">Requirements</span></span>



| <span data-ttu-id="5471d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5471d-117">Requirement</span></span> | <span data-ttu-id="5471d-118">Value</span><span class="sxs-lookup"><span data-stu-id="5471d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5471d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5471d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5471d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5471d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5471d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5471d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5471d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5471d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5471d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5471d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5471d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5471d-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5471d-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5471d-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5471d-126">**TBN \_ GETINFOTIPW** (Unicode) y **TBN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5471d-126">**TBN\_GETINFOTIPW** (Unicode) and **TBN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





