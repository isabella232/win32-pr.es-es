---
description: Especifica si el modo alfa para los tipos de vídeo en color está premultiplicado o recto.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082729"
---
# <a name="mf_mt_alpha_mode-attribute"></a><span data-ttu-id="3e121-103">\_Atributo de \_ modo alfa MF MT \_</span><span class="sxs-lookup"><span data-stu-id="3e121-103">MF\_MT\_ALPHA\_MODE attribute</span></span>

<span data-ttu-id="3e121-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="3e121-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e121-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="3e121-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e121-106">Especifica si el modo alfa para los tipos de vídeo en color está premultiplicado o recto.</span><span class="sxs-lookup"><span data-stu-id="3e121-106">Specifies whether the alpha mode for color media video types is premultiplied or straight.</span></span>

## <a name="data-type"></a><span data-ttu-id="3e121-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3e121-107">Data type</span></span>

<span data-ttu-id="3e121-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3e121-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3e121-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e121-109">Remarks</span></span>

<span data-ttu-id="3e121-110">Este valor se puede convertir en un valor de [**\_ \_ modo alfa de DXGI**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) .</span><span class="sxs-lookup"><span data-stu-id="3e121-110">This value can be cast to a [**DXGI\_ALPHA\_MODE**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) value.</span></span> <span data-ttu-id="3e121-111">Si este atributo no está presente, para la compatibilidad con versiones anteriores, el valor es el **\_ modo alfa de dxgi \_ \_ recto** para el formato de vídeo compatible con el canal alfa, como ARGB32, o el **\_ modo Alpha alfa \_ \_ omite** el formato de vídeo sin canal alfa, como RGB32.</span><span class="sxs-lookup"><span data-stu-id="3e121-111">If this attribute isn’t present, for backward compatibility, the value is **DXGI\_ALPHA\_MODE\_STRAIGHT** for video format supporting alpha channel, such as ARGB32, or **DXGI\_ALPHA\_MODE\_IGNORE** for video format without alpha channel, such as RGB32.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e121-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e121-112">Requirements</span></span>



| <span data-ttu-id="3e121-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e121-113">Requirement</span></span> | <span data-ttu-id="3e121-114">Value</span><span class="sxs-lookup"><span data-stu-id="3e121-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e121-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e121-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3e121-116">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e121-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3e121-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e121-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3e121-118">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3e121-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="3e121-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e121-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e121-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e121-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
