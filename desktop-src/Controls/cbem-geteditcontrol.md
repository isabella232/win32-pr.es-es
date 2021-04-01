---
title: Mensaje de CBEM_GETEDITCONTROL (commctrl. h)
description: Obtiene el identificador de la parte del control de edición de un control ComboBoxEx. Un control ComboBoxEx usa un cuadro de edición cuando se establece en el \_ estilo de lista desplegable CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150925"
---
# <a name="cbem_geteditcontrol-message"></a><span data-ttu-id="5a90a-105">CBEM \_ GETEDITCONTROL</span><span class="sxs-lookup"><span data-stu-id="5a90a-105">CBEM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="5a90a-106">Obtiene el identificador de la parte del control de edición de un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="5a90a-106">Gets the handle to the edit control portion of a ComboBoxEx control.</span></span> <span data-ttu-id="5a90a-107">Un control ComboBoxEx usa un cuadro de edición cuando se establece en el estilo de [**\_ lista desplegable CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5a90a-107">A ComboBoxEx control uses an edit box when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a90a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a90a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a90a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a90a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5a90a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5a90a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5a90a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a90a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5a90a-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5a90a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a90a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a90a-113">Return value</span></span>

<span data-ttu-id="5a90a-114">Devuelve el identificador del control de edición dentro del control ComboBoxEx si usa el estilo [**de \_ lista desplegable CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5a90a-114">Returns the handle to the edit control within the ComboBoxEx control if it uses the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="5a90a-115">De lo contrario, el mensaje devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5a90a-115">Otherwise, the message returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a90a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a90a-116">Requirements</span></span>



| <span data-ttu-id="5a90a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a90a-117">Requirement</span></span> | <span data-ttu-id="5a90a-118">Value</span><span class="sxs-lookup"><span data-stu-id="5a90a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a90a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a90a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5a90a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5a90a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a90a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a90a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5a90a-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a90a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a90a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a90a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a90a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a90a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





