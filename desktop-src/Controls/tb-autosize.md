---
title: Mensaje de TB_AUTOSIZE (commctrl. h)
description: Hace que se cambie el tamaño de una barra de herramientas.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- TB_AUTOSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535632"
---
# <a name="tb_autosize-message"></a><span data-ttu-id="edc01-104">\_Mensaje de tamaño automático de TB</span><span class="sxs-lookup"><span data-stu-id="edc01-104">TB\_AUTOSIZE message</span></span>

<span data-ttu-id="edc01-105">Hace que se cambie el tamaño de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="edc01-105">Causes a toolbar to be resized.</span></span>

## <a name="parameters"></a><span data-ttu-id="edc01-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edc01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc01-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edc01-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="edc01-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="edc01-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="edc01-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edc01-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="edc01-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="edc01-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc01-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edc01-111">Return value</span></span>

<span data-ttu-id="edc01-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="edc01-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edc01-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edc01-113">Remarks</span></span>

<span data-ttu-id="edc01-114">Una aplicación envía el mensaje de **tamaño de TB \_ automático** después de hacer que el tamaño de una barra de herramientas cambie estableciendo el tamaño del botón o del mapa de bits o agregando cadenas por primera vez.</span><span class="sxs-lookup"><span data-stu-id="edc01-114">An application sends the **TB\_AUTOSIZE** message after causing the size of a toolbar to change either by setting the button or bitmap size or by adding strings for the first time.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc01-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edc01-115">Requirements</span></span>



| <span data-ttu-id="edc01-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="edc01-116">Requirement</span></span> | <span data-ttu-id="edc01-117">Value</span><span class="sxs-lookup"><span data-stu-id="edc01-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edc01-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edc01-118">Minimum supported client</span></span><br/> | <span data-ttu-id="edc01-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="edc01-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edc01-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edc01-120">Minimum supported server</span></span><br/> | <span data-ttu-id="edc01-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="edc01-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edc01-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edc01-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="edc01-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="edc01-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





