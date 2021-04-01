---
title: Mensaje WM_DSA_SHEET_CREATE_NOTIFY
description: Publicado en el complemento MMC de Active Directory para crear una hoja de propiedades secundaria.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996470"
---
# <a name="wm_dsa_sheet_create_notify-message"></a><span data-ttu-id="0a81c-104">\_Creación de \_ mensaje \_ de \_ notificación de hoja DSA de WM</span><span class="sxs-lookup"><span data-stu-id="0a81c-104">WM\_DSA\_SHEET\_CREATE\_NOTIFY message</span></span>

<span data-ttu-id="0a81c-105">La **hoja de datos DSA de WM crear mensaje de \_ \_ \_ \_ notificación** se publica en el complemento MMC de Active Directory para crear una hoja de propiedades secundaria.</span><span class="sxs-lookup"><span data-stu-id="0a81c-105">The **WM\_DSA\_SHEET\_CREATE\_NOTIFY** message is posted to the Active Directory MMC snap-in to create a secondary property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="0a81c-106">Este valor de mensaje no está definido en un archivo de encabezado publicado.</span><span class="sxs-lookup"><span data-stu-id="0a81c-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="0a81c-107">Para usar este valor de mensaje, debe definirlo en el formato exacto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="0a81c-107">To use this message value, define it in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="0a81c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a81c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a81c-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="0a81c-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0a81c-110">Identificador de ventana de la ventana del complemento que procesará este mensaje.</span><span class="sxs-lookup"><span data-stu-id="0a81c-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="0a81c-111">Este identificador se obtiene del miembro **hwndHidden** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="0a81c-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a81c-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a81c-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a81c-113">Contiene un puntero a una estructura de [**\_ información de \_ página \_ de DSA sec**](dsa-sec-page-info.md) que define la hoja de propiedades secundaria que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="0a81c-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary property sheet to create.</span></span> <span data-ttu-id="0a81c-114">El receptor del mensaje debe liberar esta memoria con la función [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) cuando ya no sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="0a81c-114">The message receiver must free this memory with the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function when it is no longer required.</span></span>

</dd> <dt>

<span data-ttu-id="0a81c-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a81c-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a81c-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0a81c-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a81c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a81c-117">Return value</span></span>

<span data-ttu-id="0a81c-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0a81c-118">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a81c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a81c-119">Requirements</span></span>



| <span data-ttu-id="0a81c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a81c-120">Requirement</span></span> | <span data-ttu-id="0a81c-121">Value</span><span class="sxs-lookup"><span data-stu-id="0a81c-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0a81c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a81c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0a81c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a81c-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0a81c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a81c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0a81c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a81c-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a81c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a81c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a81c-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="0a81c-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> <dt>

[<span data-ttu-id="0a81c-128">**información de página de DSA \_ s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a81c-128">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="0a81c-129">**LocalFree**</span><span class="sxs-lookup"><span data-stu-id="0a81c-129">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

