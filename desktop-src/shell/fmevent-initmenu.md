---
description: Se envía a un archivo DLL de extensión cuando el usuario selecciona el menú de la extensión en la barra de menús del Administrador de archivos. La extensión puede usar esta notificación para inicializar elementos de menú.
title: FMEVENT_INITMENU mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 82ec9130a681bdfd36ff6259392c0608e4cde9cf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842286"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="eb60e-104">Mensaje \_ FMEVENT INITMENU</span><span class="sxs-lookup"><span data-stu-id="eb60e-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="eb60e-105">Se envía a un archivo DLL de extensión cuando el usuario selecciona el menú de la extensión en la barra de menús del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="eb60e-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="eb60e-106">La extensión puede usar esta notificación para inicializar elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="eb60e-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb60e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb60e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb60e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb60e-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eb60e-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="eb60e-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eb60e-110">*hmenu*</span><span class="sxs-lookup"><span data-stu-id="eb60e-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="eb60e-111">Identificador de la barra de menús del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="eb60e-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb60e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb60e-112">Return value</span></span>

<span data-ttu-id="eb60e-113">Un archivo DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="eb60e-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb60e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb60e-114">Remarks</span></span>

<span data-ttu-id="eb60e-115">Un archivo DLL de extensión recibe este mensaje solo cuando el usuario selecciona el menú de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="eb60e-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="eb60e-116">Si la extensión contiene submenús, debe inicializarlos al mismo tiempo que inicializa el menú de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="eb60e-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb60e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb60e-117">Requirements</span></span>



| <span data-ttu-id="eb60e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb60e-118">Requirement</span></span> | <span data-ttu-id="eb60e-119">Value</span><span class="sxs-lookup"><span data-stu-id="eb60e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb60e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb60e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eb60e-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eb60e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="eb60e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb60e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eb60e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eb60e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eb60e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb60e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb60e-125"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="eb60e-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb60e-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="eb60e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb60e-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="eb60e-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




