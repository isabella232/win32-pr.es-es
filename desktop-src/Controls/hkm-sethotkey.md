---
title: Mensaje de HKM_SETHOTKEY (commctrl. h)
description: Establece la combinación de teclas de acceso rápido de un control de tecla de acceso rápido.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534036"
---
# <a name="hkm_sethotkey-message"></a><span data-ttu-id="da6e4-104">HKM \_ SETHOTKEY</span><span class="sxs-lookup"><span data-stu-id="da6e4-104">HKM\_SETHOTKEY message</span></span>

<span data-ttu-id="da6e4-105">Establece la combinación de teclas de acceso rápido de un control de tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="da6e4-105">Sets the hot key combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="da6e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da6e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da6e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da6e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da6e4-108">El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el código de tecla virtual de la tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="da6e4-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="da6e4-109">El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de **LOWORD** es el modificador de clave que indica las teclas que definen una combinación de teclas de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="da6e4-109">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that indicates the keys that define a hot key combination.</span></span> <span data-ttu-id="da6e4-110">Para obtener una lista de valores de marcador de modificador, vea la descripción del mensaje [**\_ GETHOTKEY de HKM**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="da6e4-110">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="da6e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da6e4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da6e4-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="da6e4-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da6e4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da6e4-113">Return value</span></span>

<span data-ttu-id="da6e4-114">Siempre devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="da6e4-114">Always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="da6e4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da6e4-115">Requirements</span></span>



| <span data-ttu-id="da6e4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="da6e4-116">Requirement</span></span> | <span data-ttu-id="da6e4-117">Value</span><span class="sxs-lookup"><span data-stu-id="da6e4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da6e4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da6e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da6e4-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da6e4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da6e4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da6e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="da6e4-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="da6e4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da6e4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da6e4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="da6e4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="da6e4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

