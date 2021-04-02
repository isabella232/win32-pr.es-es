---
title: Mensaje de CB_GETCUEBANNER (Winuser. h)
description: Obtiene el texto del titular de indicación mostrado en el control de edición de un cuadro combinado. Envíe este mensaje explícitamente o mediante la \_ macro GetCueBannerText de ComboBox.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905369"
---
# <a name="cb_getcuebanner-message"></a><span data-ttu-id="0cb8b-105">\_Mensaje GETCUEBANNER CB</span><span class="sxs-lookup"><span data-stu-id="0cb8b-105">CB\_GETCUEBANNER message</span></span>

<span data-ttu-id="0cb8b-106">Obtiene el texto del titular de indicación mostrado en el control de edición de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-106">Gets the cue banner text displayed in the edit control of a combo box.</span></span> <span data-ttu-id="0cb8b-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetCueBannerText de ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .</span><span class="sxs-lookup"><span data-stu-id="0cb8b-107">Send this message explicitly or by using the [**ComboBox\_GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cb8b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cb8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb8b-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cb8b-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb8b-110">Un puntero a un búfer de cadena Unicode que recibe el texto del titular de indicación.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-110">A pointer to a Unicode string buffer that receives the cue banner text.</span></span> <span data-ttu-id="0cb8b-111">La aplicación que realiza la llamada es responsable de asignar la memoria para el búfer.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-111">The calling application is responsible for allocating the memory for the buffer.</span></span> <span data-ttu-id="0cb8b-112">El tamaño del búfer debe ser igual a la longitud de la cadena de banner de indicación en **WCHARs**, además de 1 para el **WCHAR** **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-112">The buffer size must be equal to the length of the cue banner string in **WCHARs**, plus 1 for the terminating **NULL** **WCHAR**.</span></span>

</dd> <dt>

<span data-ttu-id="0cb8b-113">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cb8b-113">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb8b-114">Tamaño del búfer al que apunta *lpcwText* en **WCHARs**.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-114">The size of the buffer pointed to by *lpcwText* in **WCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb8b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cb8b-115">Return value</span></span>

<span data-ttu-id="0cb8b-116">Devuelve 1 si se realiza correctamente, o un valor de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-116">Returns 1 if successful, or an error value otherwise.</span></span>

<span data-ttu-id="0cb8b-117">Si no hay ningún texto de titular de indicación para obtener, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-117">If there is no cue banner text to get, the return value is 0.</span></span> <span data-ttu-id="0cb8b-118">Si la aplicación que realiza la llamada no puede asignar un búfer o establece *lParam* antes de enviar este mensaje, podría producirse un comportamiento indefinido y es posible que el valor devuelto no sea confiable.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-118">If the calling application fails to allocate a buffer, or set *lParam* before sending this message, undefined behavior may result and the return value may not be reliable.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb8b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb8b-119">Requirements</span></span>



| <span data-ttu-id="0cb8b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb8b-120">Requirement</span></span> | <span data-ttu-id="0cb8b-121">Value</span><span class="sxs-lookup"><span data-stu-id="0cb8b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb8b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cb8b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb8b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0cb8b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0cb8b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cb8b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb8b-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0cb8b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0cb8b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cb8b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb8b-127"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb8b-127"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb8b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cb8b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb8b-129">Características del cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="0cb8b-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





