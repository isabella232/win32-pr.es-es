---
title: Mensaje de TB_HASACCELERATOR (commctrl. h)
description: Recupera un recuento de botones de la barra de herramientas que tienen el carácter de aceleración especificado.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490996"
---
# <a name="tb_hasaccelerator-message"></a><span data-ttu-id="ba264-104">\_Mensaje HASACCELERATOR TB</span><span class="sxs-lookup"><span data-stu-id="ba264-104">TB\_HASACCELERATOR message</span></span>

<span data-ttu-id="ba264-105">\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</span><span class="sxs-lookup"><span data-stu-id="ba264-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="ba264-106">Es posible que este mensaje no se admita en versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ba264-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="ba264-107">Recupera un recuento de botones de la barra de herramientas que tienen el carácter de aceleración especificado.</span><span class="sxs-lookup"><span data-stu-id="ba264-107">Retrieves a count of toolbar buttons that have the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba264-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba264-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba264-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba264-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba264-110">**WCHAR** que representa el carácter de acelerador de entrada que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="ba264-110">A **WCHAR** representing the input accelerator character to test.</span></span>

</dd> <dt>

<span data-ttu-id="ba264-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba264-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba264-112">Puntero a un valor **int** que recibe el número de botones que tienen el carácter de acelerador.</span><span class="sxs-lookup"><span data-stu-id="ba264-112">Pointer to an **int** that receives the number of buttons that have the accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba264-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba264-113">Return value</span></span>

<span data-ttu-id="ba264-114">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ba264-114">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="ba264-115">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="ba264-115">Security Considerations</span></span>

<span data-ttu-id="ba264-116">El uso de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="ba264-116">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba264-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba264-117">Remarks</span></span>

<span data-ttu-id="ba264-118">En primer lugar, el sistema consulta todos los botones de la barra de herramientas para los aceleradores coincidentes.</span><span class="sxs-lookup"><span data-stu-id="ba264-118">First, the system queries all toolbar buttons for matching accelerators.</span></span> <span data-ttu-id="ba264-119">Si no se encuentran coincidencias, el sistema envía la notificación [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) a la ventana primaria, solicitando el índice del botón que tiene el carácter de aceleración especificado.</span><span class="sxs-lookup"><span data-stu-id="ba264-119">If no matches are found, the system sends the [TBN\_MAPACCELERATOR](tbn-mapaccelerator.md) notification to the parent window, requesting the index of the button that has the specified accelerator character.</span></span> <span data-ttu-id="ba264-120">Si el elemento primario proporciona un índice, el recuento se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="ba264-120">If the parent provides an index, the count is set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba264-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba264-121">Requirements</span></span>



| <span data-ttu-id="ba264-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba264-122">Requirement</span></span> | <span data-ttu-id="ba264-123">Value</span><span class="sxs-lookup"><span data-stu-id="ba264-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba264-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba264-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ba264-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ba264-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba264-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba264-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ba264-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba264-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba264-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba264-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba264-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba264-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





