---
description: Especifica que el descodificador debe reenviar los tipos de unidad de la capa de abstracción de red (NAL) en los ejemplos de salida.
ms.assetid: 2A1D8629-EB66-4F72-9AD7-93123D941BB0
title: MF_MT_FORWARD_CUSTOM_NALU atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a318523f52ab7d65450c4c2f35b7bfbf63d5f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546622"
---
# <a name="mf_mt_forward_custom_nalu-attribute"></a><span data-ttu-id="d731e-103">\_ \_ \_ Atributo Nalu personalizado MF MT Forward \_</span><span class="sxs-lookup"><span data-stu-id="d731e-103">MF\_MT\_FORWARD\_CUSTOM\_NALU attribute</span></span>

<span data-ttu-id="d731e-104">Especifica que el descodificador debe reenviar los tipos de unidad de la capa de abstracción de red (NAL) en los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="d731e-104">Specifies that network abstraction layer (NAL) unit types should be forwarded on output samples by the decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="d731e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d731e-105">Data type</span></span>

<span data-ttu-id="d731e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d731e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d731e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d731e-107">Remarks</span></span>

<span data-ttu-id="d731e-108">Si el descodificador analiza un NALU, no se reenviará.</span><span class="sxs-lookup"><span data-stu-id="d731e-108">If the decoder parses a NALU then it will not be forwarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="d731e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d731e-109">Requirements</span></span>



| <span data-ttu-id="d731e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d731e-110">Requirement</span></span> | <span data-ttu-id="d731e-111">Value</span><span class="sxs-lookup"><span data-stu-id="d731e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d731e-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d731e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d731e-113">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d731e-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d731e-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d731e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d731e-115">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="d731e-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d731e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d731e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d731e-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d731e-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




