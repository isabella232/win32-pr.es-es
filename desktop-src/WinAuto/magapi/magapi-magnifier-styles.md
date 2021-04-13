---
title: Estilos del ampliador
description: En este tema se describen los estilos utilizados con el control ampliador.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422330"
---
# <a name="magnifier-styles"></a><span data-ttu-id="e1435-103">Estilos del ampliador</span><span class="sxs-lookup"><span data-stu-id="e1435-103">Magnifier Styles</span></span>

<span data-ttu-id="e1435-104">En este tema se describen los estilos utilizados con el control ampliador.</span><span class="sxs-lookup"><span data-stu-id="e1435-104">This topic describes the styles used with the magnifier control.</span></span> <span data-ttu-id="e1435-105">Para crear un control ampliador, utilice la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) y especifique la clase de ventana WC_MAGNIFIER, junto con una combinación de los siguientes estilos del ampliador.</span><span class="sxs-lookup"><span data-stu-id="e1435-105">To create a magnifier control, use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function and specify the WC_MAGNIFIER window class, along with a combination of the following magnifier styles.</span></span>

| <span data-ttu-id="e1435-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1435-106">Requirement</span></span> | <span data-ttu-id="e1435-107">Value</span><span class="sxs-lookup"><span data-stu-id="e1435-107">Value</span></span> |
|:---|:---|
| <span data-ttu-id="e1435-108">MS_CLIPAROUNDCURSOR 0x0002L</span><span class="sxs-lookup"><span data-stu-id="e1435-108">MS_CLIPAROUNDCURSOR 0x0002L</span></span> | <span data-ttu-id="e1435-109">Recorta el área de la ventana del ampliador que rodea el cursor del sistema.</span><span class="sxs-lookup"><span data-stu-id="e1435-109">Clips the area of the magnifier window that surrounds the system cursor.</span></span> <span data-ttu-id="e1435-110">Este estilo permite al usuario ver el contenido de la pantalla que está detrás de la ventana del ampliador.</span><span class="sxs-lookup"><span data-stu-id="e1435-110">This style enables the user to see screen content that is behind the magnifier window.</span></span> |
| <span data-ttu-id="e1435-111">MS_INVERTCOLORS 0x0004L</span><span class="sxs-lookup"><span data-stu-id="e1435-111">MS_INVERTCOLORS 0x0004L</span></span> | <span data-ttu-id="e1435-112">Muestra el contenido de la pantalla ampliada con colores invertidos.</span><span class="sxs-lookup"><span data-stu-id="e1435-112">Displays the magnified screen content using inverted colors.</span></span> |
| <span data-ttu-id="e1435-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span><span class="sxs-lookup"><span data-stu-id="e1435-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span></span> | <span data-ttu-id="e1435-114">Muestra el cursor del sistema ampliado junto con el contenido de la pantalla ampliada.</span><span class="sxs-lookup"><span data-stu-id="e1435-114">Displays the magnified system cursor along with the magnified screen content.</span></span> |

## <a name="requirements"></a><span data-ttu-id="e1435-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1435-115">Requirements</span></span>

| <span data-ttu-id="e1435-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1435-116">Requirement</span></span> | <span data-ttu-id="e1435-117">Value</span><span class="sxs-lookup"><span data-stu-id="e1435-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1435-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1435-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1435-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e1435-119">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e1435-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1435-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1435-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1435-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e1435-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1435-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1435-123"><dt>Aumento de tamaño. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1435-123"><dt>Magnification.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e1435-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1435-124">See also</span></span>

[<span data-ttu-id="e1435-125">Constantes</span><span class="sxs-lookup"><span data-stu-id="e1435-125">Constants</span></span>](entry-magapi-constants.md)
