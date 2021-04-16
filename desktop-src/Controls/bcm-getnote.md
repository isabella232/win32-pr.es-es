---
title: Mensaje de BCM_GETNOTE (commctrl. h)
description: Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetNote.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658214"
---
# <a name="bcm_getnote-message"></a><span data-ttu-id="1fcb1-105">\_Mensaje GETNOTE de BCM</span><span class="sxs-lookup"><span data-stu-id="1fcb1-105">BCM\_GETNOTE message</span></span>

<span data-ttu-id="1fcb1-106">Obtiene el texto de la nota asociada a un botón de vínculo de comando.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-106">Gets the text of the note associated with a command link button.</span></span> <span data-ttu-id="1fcb1-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .</span><span class="sxs-lookup"><span data-stu-id="1fcb1-107">You can send this message explicitly or use the [**Button\_GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1fcb1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fcb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fcb1-109">*wParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1fcb1-109">*wParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcb1-110">**DWORD** que especifica el tamaño del búfer señalado por *lParam*, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-110">A **DWORD** that specifies the size of the buffer pointed to by *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="1fcb1-111">*lParam* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1fcb1-111">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcb1-112">Búfer de cadena para recibir el texto.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-112">The string buffer to receive the text.</span></span> <span data-ttu-id="1fcb1-113">El búfer debe ser lo suficientemente grande como para dar cabida al carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-113">The buffer must be large enough to accommodate the terminating NULL character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fcb1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fcb1-114">Return value</span></span>

<span data-ttu-id="1fcb1-115">Si el mensaje se realiza correctamente, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-115">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="1fcb1-116">En caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-116">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fcb1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fcb1-117">Remarks</span></span>

<span data-ttu-id="1fcb1-118">El **mensaje \_ GETNOTE de BCM** solo funciona con los botones que tienen el estilo de botón [**BS \_ COMMANDLINK**](button-styles.md) o [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcb1-118">The **BCM\_GETNOTE** message works only with buttons that have the [**BS\_COMMANDLINK**](button-styles.md) or [**BS\_DEFCOMMANDLINK**](button-styles.md) button style.</span></span>

<span data-ttu-id="1fcb1-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) contendrá:</span><span class="sxs-lookup"><span data-stu-id="1fcb1-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will contain:</span></span>

-   <span data-ttu-id="1fcb1-120">ERROR \_ no \_ compatible, si el botón no tiene el estilo [**BS \_ DEFCOMMANDLINK**](button-styles.md) o [**BS \_ COMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcb1-120">ERROR\_NOT\_SUPPORTED, if the button does not have the [**BS\_DEFCOMMANDLINK**](button-styles.md) or [**BS\_COMMANDLINK**](button-styles.md) style.</span></span>
-   <span data-ttu-id="1fcb1-121">ERROR \_ de \_ búfer insuficiente, si el búfer *lParam* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-121">ERROR\_INSUFFICIENT\_BUFFER, if the *lParam* buffer is too small.</span></span> <span data-ttu-id="1fcb1-122">El parámetro *wParam* contendrá el tamaño de búfer necesario, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-122">The *wParam* parameter will contain the required buffer size, in characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcb1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fcb1-123">Requirements</span></span>



| <span data-ttu-id="1fcb1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcb1-124">Requirement</span></span> | <span data-ttu-id="1fcb1-125">Value</span><span class="sxs-lookup"><span data-stu-id="1fcb1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcb1-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fcb1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1fcb1-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1fcb1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1fcb1-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fcb1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1fcb1-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fcb1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1fcb1-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fcb1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fcb1-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fcb1-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fcb1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fcb1-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="1fcb1-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1fcb1-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1fcb1-134">Estilos de botón</span><span class="sxs-lookup"><span data-stu-id="1fcb1-134">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="1fcb1-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1fcb1-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1fcb1-136">Tipos de botón</span><span class="sxs-lookup"><span data-stu-id="1fcb1-136">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

