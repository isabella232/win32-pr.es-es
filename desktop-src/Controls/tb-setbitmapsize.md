---
title: Mensaje de TB_SETBITMAPSIZE (commctrl. h)
description: Establece el tamaño de las imágenes de mapa de imágenes que se van a agregar a una barra de herramientas.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- TB_SETBITMAPSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489029"
---
# <a name="tb_setbitmapsize-message"></a><span data-ttu-id="380aa-104">\_Mensaje SETBITMAPSIZE TB</span><span class="sxs-lookup"><span data-stu-id="380aa-104">TB\_SETBITMAPSIZE message</span></span>

<span data-ttu-id="380aa-105">Establece el tamaño de las imágenes de mapa de imágenes que se van a agregar a una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="380aa-105">Sets the size of the bitmapped images to be added to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="380aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="380aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="380aa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="380aa-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="380aa-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="380aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="380aa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="380aa-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el ancho, en píxeles, de las imágenes de mapa de bytes.</span><span class="sxs-lookup"><span data-stu-id="380aa-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the bitmapped images.</span></span> <span data-ttu-id="380aa-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el alto, en píxeles, de las imágenes de mapa Dete.</span><span class="sxs-lookup"><span data-stu-id="380aa-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the bitmapped images.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380aa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="380aa-112">Return value</span></span>

<span data-ttu-id="380aa-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="380aa-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="380aa-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="380aa-114">Remarks</span></span>

<span data-ttu-id="380aa-115">Solo se puede establecer el tamaño antes de agregar mapas de bits a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="380aa-115">The size can be set only before adding any bitmaps to the toolbar.</span></span> <span data-ttu-id="380aa-116">Si una aplicación no establece explícitamente el tamaño del mapa de bits, el tamaño predeterminado es de 16 por 15 píxeles.</span><span class="sxs-lookup"><span data-stu-id="380aa-116">If an application does not explicitly set the bitmap size, the size defaults to 16 by 15 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="380aa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="380aa-117">Requirements</span></span>



| <span data-ttu-id="380aa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="380aa-118">Requirement</span></span> | <span data-ttu-id="380aa-119">Value</span><span class="sxs-lookup"><span data-stu-id="380aa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="380aa-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="380aa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="380aa-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="380aa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="380aa-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="380aa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="380aa-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="380aa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="380aa-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="380aa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="380aa-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="380aa-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

