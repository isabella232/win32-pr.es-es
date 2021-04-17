---
title: Mensaje WM_ADSPROP_SHEET_CREATE
description: Se envía al objeto de notificación para crear una hoja de propiedades secundaria en un complemento MMC de Active Directory.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_SHEET_CREATE Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534222"
---
# <a name="wm_adsprop_sheet_create-message"></a><span data-ttu-id="2ef0b-104">\_ \_ Crear mensaje de hoja de ADSPROP de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ef0b-104">WM\_ADSPROP\_SHEET\_CREATE message</span></span>

<span data-ttu-id="2ef0b-105">El mensaje de creación de la hoja de ADSPROP de WM se envía al objeto de notificación para crear una hoja de propiedades secundaria en un complemento de MMC de Active Directory. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ef0b-105">The **WM\_ADSPROP\_SHEET\_CREATE** message is sent to the notification object to create a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="2ef0b-106">Este valor de mensaje no está definido en un archivo de encabezado publicado.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="2ef0b-107">Para usar este valor de mensaje, debe definirlo en el formato exacto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="2ef0b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ef0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef0b-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="2ef0b-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2ef0b-110">Identificador del objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-110">The handle of the notification object.</span></span> <span data-ttu-id="2ef0b-111">Para obtener este identificador, llame a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="2ef0b-111">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="2ef0b-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ef0b-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ef0b-113">Contiene un puntero a una estructura de [**\_ información de \_ página \_ de DSA sec**](dsa-sec-page-info.md) que define la página secundaria que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary page to create.</span></span> <span data-ttu-id="2ef0b-114">Solo se puede crear una hoja de propiedades secundaria con **la \_ hoja de ADSPROP de WM \_ \_ Create** Message, por lo que la estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) solo puede contener una estructura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="2ef0b-114">Only one secondary property sheet can be created with the **WM\_ADSPROP\_SHEET\_CREATE** message, so the [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2ef0b-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ef0b-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ef0b-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-116">Not used.</span></span> <span data-ttu-id="2ef0b-117">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-117">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef0b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ef0b-118">Return value</span></span>

<span data-ttu-id="2ef0b-119">El valor devuelto para este mensaje es siempre cero.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-119">The return value for this message is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef0b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ef0b-120">Remarks</span></span>

<span data-ttu-id="2ef0b-121">El autor de la llamada debe asignar la estructura de [**información de página de DSA \_ \_ \_ sec**](dsa-sec-page-info.md) , la cadena de título y todas las cadenas de [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) con una sola llamada a la función [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) .</span><span class="sxs-lookup"><span data-stu-id="2ef0b-121">The caller must allocate the [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure, the title string and all [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) strings using a single call to the [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) function.</span></span> <span data-ttu-id="2ef0b-122">El mensaje de creación de la **\_ \_ hoja \_ ADSPROP de WM** es un mensaje asincrónico, por lo que se devolverá antes de crear la hoja secundaria.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-122">The **WM\_ADSPROP\_SHEET\_CREATE** message is an asynchronous message, so it will return before the secondary sheet is created.</span></span> <span data-ttu-id="2ef0b-123">Por este motivo, la memoria debe permanecer intacta después de que el mensaje se devuelva.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-123">Because of this, the memory must remain intact after the message returns.</span></span> <span data-ttu-id="2ef0b-124">El receptor liberará esta memoria con una sola llamada a la función [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) una vez creada la hoja secundaria.</span><span class="sxs-lookup"><span data-stu-id="2ef0b-124">The receiver will free this memory with a single call to the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function after the secondary sheet is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef0b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ef0b-125">Requirements</span></span>



| <span data-ttu-id="2ef0b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ef0b-126">Requirement</span></span> | <span data-ttu-id="2ef0b-127">Value</span><span class="sxs-lookup"><span data-stu-id="2ef0b-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2ef0b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ef0b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2ef0b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ef0b-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2ef0b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ef0b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2ef0b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ef0b-131">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ef0b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ef0b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef0b-133">**CFSTR \_ DS \_ PARENTHWND**</span><span class="sxs-lookup"><span data-stu-id="2ef0b-133">**CFSTR\_DS\_PARENTHWND**</span></span>](cfstr-ds-parenthwnd.md)
</dt> <dt>

[<span data-ttu-id="2ef0b-134">**información de página de DSA \_ s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ef0b-134">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="2ef0b-135">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="2ef0b-135">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="2ef0b-136">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="2ef0b-136">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[<span data-ttu-id="2ef0b-137">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="2ef0b-137">**LocalAlloc**</span></span>](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[<span data-ttu-id="2ef0b-138">**LocalFree**</span><span class="sxs-lookup"><span data-stu-id="2ef0b-138">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

