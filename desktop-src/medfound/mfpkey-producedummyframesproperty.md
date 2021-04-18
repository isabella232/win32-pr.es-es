---
description: Especifica si el codificador genera entradas de fotogramas ficticias en el flujo de bits para los fotogramas duplicados.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: Propiedad MFPKEY_PRODUCEDUMMYFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276307"
---
# <a name="mfpkey_producedummyframes-property"></a><span data-ttu-id="53afe-103">\_Propiedad PRODUCEDUMMYFRAMES de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="53afe-103">MFPKEY\_PRODUCEDUMMYFRAMES Property</span></span>

<span data-ttu-id="53afe-104">Especifica si el codificador genera entradas de fotogramas ficticias en el flujo de bits para los fotogramas duplicados.</span><span class="sxs-lookup"><span data-stu-id="53afe-104">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="53afe-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="53afe-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="53afe-106">g \_ wszWMVCProduceDummyFrames</span><span class="sxs-lookup"><span data-stu-id="53afe-106">g\_wszWMVCProduceDummyFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="53afe-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="53afe-107">Data Type</span></span>

<span data-ttu-id="53afe-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="53afe-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="53afe-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="53afe-109">Default Value</span></span>

<span data-ttu-id="53afe-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="53afe-110">VARIANT\_FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="53afe-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53afe-111">Remarks</span></span>

<span data-ttu-id="53afe-112">Si este valor es VARIANT \_ false, el códec no colocará ningún dato en el flujo de bits para los fotogramas duplicados.</span><span class="sxs-lookup"><span data-stu-id="53afe-112">If this value is VARIANT\_FALSE, the codec will not put any data in the bit stream for duplicate frames.</span></span>

<span data-ttu-id="53afe-113">Los marcos ficticios pueden ser importantes en las aplicaciones donde se conservan los números de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="53afe-113">Dummy frames can be important in applications where frame numbers are persisted.</span></span> <span data-ttu-id="53afe-114">Un ejemplo común es cuando se mantienen códigos de tiempo SMPTE para contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="53afe-114">A common example is when SMPTE time codes are maintained for encoded content.</span></span>

## <a name="requirements"></a><span data-ttu-id="53afe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53afe-115">Requirements</span></span>



| <span data-ttu-id="53afe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="53afe-116">Requirement</span></span> | <span data-ttu-id="53afe-117">Value</span><span class="sxs-lookup"><span data-stu-id="53afe-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53afe-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53afe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53afe-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="53afe-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="53afe-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53afe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53afe-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="53afe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="53afe-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53afe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="53afe-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="53afe-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53afe-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="53afe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53afe-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53afe-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




