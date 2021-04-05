---
title: Código de notificación de TBN_DUPACCELERATOR (commctrl. h)
description: Determina si se puede usar una tecla de aceleración en dos o más barras de herramientas activas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079601"
---
# <a name="tbn_dupaccelerator-notification-code"></a><span data-ttu-id="ba5c7-105">Código de notificación de DUPACCELERATOR de TBN \_</span><span class="sxs-lookup"><span data-stu-id="ba5c7-105">TBN\_DUPACCELERATOR notification code</span></span>

<span data-ttu-id="ba5c7-106">Determina si se puede usar una tecla de aceleración en dos o más barras de herramientas activas.</span><span class="sxs-lookup"><span data-stu-id="ba5c7-106">Ascertains whether an accelerator key can be used on two or more active toolbars.</span></span> <span data-ttu-id="ba5c7-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ba5c7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ba5c7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba5c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba5c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba5c7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba5c7-110">Puntero a una estructura que proporciona un acelerador y que recibe un valor que especifica si varias barras de herramientas responden al mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="ba5c7-110">A pointer to a structure that provides an accelerator and that receives a value specifying whether multiple toolbars respond to the same character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba5c7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba5c7-111">Return value</span></span>

<span data-ttu-id="ba5c7-112">Devuelve **true** si es correcto; de lo contrario, **es false**.</span><span class="sxs-lookup"><span data-stu-id="ba5c7-112">Returns **TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba5c7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba5c7-113">Remarks</span></span>

<span data-ttu-id="ba5c7-114">La aplicación debe declarar la estructura **NMTBDUPACCELERATOR** como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ba5c7-114">The application must declare the **NMTBDUPACCELERATOR** structure as follows:</span></span>

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="ba5c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba5c7-115">Requirements</span></span>



| <span data-ttu-id="ba5c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba5c7-116">Requirement</span></span> | <span data-ttu-id="ba5c7-117">Value</span><span class="sxs-lookup"><span data-stu-id="ba5c7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5c7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba5c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5c7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ba5c7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba5c7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba5c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5c7-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba5c7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba5c7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba5c7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba5c7-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba5c7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





