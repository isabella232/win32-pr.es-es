---
title: Mensaje de SB_GETTIPTEXT (commctrl. h)
description: Recupera el texto de información sobre herramientas de un elemento de una barra de estado. La barra de estado se debe crear con el \_ estilo de información sobre herramientas de SBT para habilitar la información sobre herramientas.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905458"
---
# <a name="sb_gettiptext-message"></a><span data-ttu-id="d56b9-105">\_Mensaje GETTIPTEXT de SB</span><span class="sxs-lookup"><span data-stu-id="d56b9-105">SB\_GETTIPTEXT message</span></span>

<span data-ttu-id="d56b9-106">Recupera el texto de información sobre herramientas de un elemento de una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="d56b9-106">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="d56b9-107">La barra de estado se debe crear con el estilo de [**\_ información sobre herramientas de SBT**](status-bar-styles.md) para habilitar la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="d56b9-107">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="d56b9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d56b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d56b9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d56b9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d56b9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el índice de base cero del elemento que recibe el texto de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="d56b9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the part that receives the tooltip text.</span></span> <span data-ttu-id="d56b9-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el tamaño del búfer en *lParam*, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="d56b9-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the size of the buffer at *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="d56b9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d56b9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d56b9-113">Puntero a un búfer de caracteres que recibe el texto de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="d56b9-113">Pointer to a character buffer that receives the tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d56b9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d56b9-114">Return value</span></span>

<span data-ttu-id="d56b9-115">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d56b9-115">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d56b9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d56b9-116">Remarks</span></span>

<span data-ttu-id="d56b9-117">**Advertencia de seguridad:** El uso incorrecto de este mensaje puede producir problemas en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d56b9-117">**Security Warning:** Using this message incorrectly can cause problems for your application.</span></span> <span data-ttu-id="d56b9-118">Por ejemplo, si el texto es demasiado grande para el búfer *lParam* , podría producirse un desbordamiento del búfer.</span><span class="sxs-lookup"><span data-stu-id="d56b9-118">For example, if the text is too large for the *lParam* buffer, it could cause a buffer overflow.</span></span> <span data-ttu-id="d56b9-119">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="d56b9-119">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d56b9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d56b9-120">Requirements</span></span>



| <span data-ttu-id="d56b9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d56b9-121">Requirement</span></span> | <span data-ttu-id="d56b9-122">Value</span><span class="sxs-lookup"><span data-stu-id="d56b9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d56b9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d56b9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d56b9-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d56b9-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d56b9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d56b9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d56b9-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d56b9-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d56b9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d56b9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d56b9-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d56b9-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d56b9-129">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d56b9-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d56b9-130">**SB \_ GETTIPTEXTW** (Unicode) y **SB \_ GETTIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d56b9-130">**SB\_GETTIPTEXTW** (Unicode) and **SB\_GETTIPTEXTA** (ANSI)</span></span><br/>               |



 

