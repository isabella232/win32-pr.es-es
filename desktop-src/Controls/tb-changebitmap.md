---
title: Mensaje de TB_CHANGEBITMAP (commctrl. h)
description: Cambia el mapa de bits de un botón de una barra de herramientas.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905685"
---
# <a name="tb_changebitmap-message"></a><span data-ttu-id="b6d46-104">\_Mensaje CHANGEBITMAP TB</span><span class="sxs-lookup"><span data-stu-id="b6d46-104">TB\_CHANGEBITMAP message</span></span>

<span data-ttu-id="b6d46-105">Cambia el mapa de bits de un botón de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b6d46-105">Changes the bitmap for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6d46-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6d46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6d46-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6d46-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6d46-108">Identificador de comando del botón que va a recibir un nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="b6d46-108">Command identifier of the button that is to receive a new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="b6d46-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6d46-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6d46-110">Índice de base cero de una imagen en la lista de imágenes de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b6d46-110">Zero-based index of an image in the toolbar's image list.</span></span> <span data-ttu-id="b6d46-111">El sistema muestra la imagen especificada en el botón.</span><span class="sxs-lookup"><span data-stu-id="b6d46-111">The system displays the specified image in the button.</span></span> <span data-ttu-id="b6d46-112">Establezca este parámetro en I \_ IMAGECALLBACK y la barra de herramientas enviará la notificación [**TBN \_ GETDISPINFO**](tbn-getdispinfo.md) para recuperar el índice de la imagen cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b6d46-112">Set this parameter to I\_IMAGECALLBACK, and the toolbar will send the [**TBN\_GETDISPINFO**](tbn-getdispinfo.md) notification to retrieve the image index when it is needed.</span></span>

<span data-ttu-id="b6d46-113">[Versión 5,81](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="b6d46-113">[Version 5.81](common-control-versions.md).</span></span> <span data-ttu-id="b6d46-114">Establezca este parámetro en I \_ IMAGENONE para indicar que el botón no tiene una imagen.</span><span class="sxs-lookup"><span data-stu-id="b6d46-114">Set this parameter to I\_IMAGENONE to indicate that the button does not have an image.</span></span> <span data-ttu-id="b6d46-115">El diseño del botón no incluirá ningún espacio para un mapa de bits, solo texto.</span><span class="sxs-lookup"><span data-stu-id="b6d46-115">The button layout will not include any space for a bitmap, only text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6d46-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6d46-116">Return value</span></span>

<span data-ttu-id="b6d46-117">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b6d46-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6d46-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6d46-118">Requirements</span></span>



| <span data-ttu-id="b6d46-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6d46-119">Requirement</span></span> | <span data-ttu-id="b6d46-120">Value</span><span class="sxs-lookup"><span data-stu-id="b6d46-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d46-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6d46-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6d46-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b6d46-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6d46-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6d46-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6d46-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6d46-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6d46-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6d46-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6d46-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6d46-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





