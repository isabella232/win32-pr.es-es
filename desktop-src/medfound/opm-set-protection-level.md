---
description: Establece el nivel de protección de un mecanismo de protección de la salida.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715521"
---
# <a name="opm_set_protection_level"></a><span data-ttu-id="a15b4-103">\_nivel de \_ protección de conjunto de OPM \_</span><span class="sxs-lookup"><span data-stu-id="a15b4-103">OPM\_SET\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="a15b4-104">Establece el nivel de protección de un mecanismo de protección de la salida.</span><span class="sxs-lookup"><span data-stu-id="a15b4-104">Sets the protection level for an output protection mechanism.</span></span>



| <span data-ttu-id="a15b4-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="a15b4-105">Requirement</span></span> | <span data-ttu-id="a15b4-106">Value</span><span class="sxs-lookup"><span data-stu-id="a15b4-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a15b4-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="a15b4-107">Command GUID</span></span> | <span data-ttu-id="a15b4-108">\_nivel de \_ protección de conjunto de OPM \_</span><span class="sxs-lookup"><span data-stu-id="a15b4-108">OPM\_SET\_PROTECTION\_LEVEL</span></span>                                                                         |
| <span data-ttu-id="a15b4-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="a15b4-109">Input data</span></span>   | <span data-ttu-id="a15b4-110">Una estructura de [**parámetros de nivel de protección de \_ configuración \_ \_ \_ de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="a15b4-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a15b4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a15b4-111">Remarks</span></span>

<span data-ttu-id="a15b4-112">Algunos conectores pueden admitir varios mecanismos de protección.</span><span class="sxs-lookup"><span data-stu-id="a15b4-112">Some connectors can support multiple protection mechanisms.</span></span> <span data-ttu-id="a15b4-113">Con ese tipo de conector, puede aplicar varios mecanismos de protección al mismo conector, con una configuración diferente para cada uno.</span><span class="sxs-lookup"><span data-stu-id="a15b4-113">With that type of connector, you can apply several protection mechanisms to the same connector, with different settings for each.</span></span>

## <a name="requirements"></a><span data-ttu-id="a15b4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a15b4-114">Requirements</span></span>



| <span data-ttu-id="a15b4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a15b4-115">Requirement</span></span> | <span data-ttu-id="a15b4-116">Value</span><span class="sxs-lookup"><span data-stu-id="a15b4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a15b4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a15b4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a15b4-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a15b4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a15b4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a15b4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a15b4-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a15b4-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a15b4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a15b4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a15b4-122"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a15b4-122"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a15b4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a15b4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a15b4-124">**IOPMVideoOutput:: configure**</span><span class="sxs-lookup"><span data-stu-id="a15b4-124">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="a15b4-125">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="a15b4-125">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




