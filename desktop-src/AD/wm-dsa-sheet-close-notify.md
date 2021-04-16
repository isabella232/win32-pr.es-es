---
title: Mensaje WM_DSA_SHEET_CLOSE_NOTIFY
description: Se publica en el complemento MMC de Active Directory cuando se destruye una hoja de propiedades secundaria.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658217"
---
# <a name="wm_dsa_sheet_close_notify-message"></a><span data-ttu-id="9d562-104">\_Mensaje de \_ \_ notificación de cierre de hoja DSA de WM \_</span><span class="sxs-lookup"><span data-stu-id="9d562-104">WM\_DSA\_SHEET\_CLOSE\_NOTIFY message</span></span>

<span data-ttu-id="9d562-105">El mensaje de **\_ notificación de \_ \_ cierre \_ de hoja DSA de WM** se envía al complemento MMC de Active Directory cuando se destruye una hoja de propiedades secundaria.</span><span class="sxs-lookup"><span data-stu-id="9d562-105">The **WM\_DSA\_SHEET\_CLOSE\_NOTIFY** message is posted to the Active Directory MMC snap-in when a secondary property sheet is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="9d562-106">Este valor de mensaje no está definido en un archivo de encabezado publicado.</span><span class="sxs-lookup"><span data-stu-id="9d562-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="9d562-107">Para usar este valor de mensaje, debe definirlo en el formato exacto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="9d562-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="9d562-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d562-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d562-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="9d562-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9d562-110">Identificador de ventana de la ventana del complemento que procesará este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9d562-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="9d562-111">Este identificador se obtiene del miembro **hwndHidden** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="9d562-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9d562-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d562-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d562-113">Contiene un valor de 32 bits definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d562-113">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="9d562-114">Esto se obtiene del miembro **wParamSheetClose** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="9d562-114">This is obtained from the **wParamSheetClose** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9d562-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d562-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d562-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9d562-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d562-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d562-117">Return value</span></span>

<span data-ttu-id="9d562-118">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9d562-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d562-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d562-119">Requirements</span></span>



| <span data-ttu-id="9d562-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d562-120">Requirement</span></span> | <span data-ttu-id="9d562-121">Value</span><span class="sxs-lookup"><span data-stu-id="9d562-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9d562-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d562-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9d562-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d562-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9d562-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d562-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9d562-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d562-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d562-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d562-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d562-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="9d562-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> </dl>

 

 





