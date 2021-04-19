---
description: Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: Propiedad MFPKEY_CODEDNONZEROFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716037"
---
# <a name="mfpkey_codednonzeroframes-property"></a><span data-ttu-id="04b9a-103">\_Propiedad CODEDNONZEROFRAMES de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="04b9a-103">MFPKEY\_CODEDNONZEROFRAMES Property</span></span>

<span data-ttu-id="04b9a-104">Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.</span><span class="sxs-lookup"><span data-stu-id="04b9a-104">Specifies the number of video frames encoded by the codec that actually contain data.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="04b9a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="04b9a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="04b9a-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="04b9a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="04b9a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="04b9a-107">Data Type</span></span>

<span data-ttu-id="04b9a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="04b9a-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="04b9a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04b9a-109">Remarks</span></span>

<span data-ttu-id="04b9a-110">Este valor es igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos cualquier fotograma que se haya quitado debido a restricciones de velocidad de bits, menos cualquier trama de cero bytes.</span><span class="sxs-lookup"><span data-stu-id="04b9a-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints, minus any zero-byte frames.</span></span> <span data-ttu-id="04b9a-111">Puede obtener este valor después de haber terminado de pasar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="04b9a-111">You can get this value after you are finished passing samples.</span></span> <span data-ttu-id="04b9a-112">Los fotogramas de cero bytes se pueden crear para fotogramas duplicados.</span><span class="sxs-lookup"><span data-stu-id="04b9a-112">Zero-byte frames can be created for duplicate frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b9a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04b9a-113">Requirements</span></span>



| <span data-ttu-id="04b9a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b9a-114">Requirement</span></span> | <span data-ttu-id="04b9a-115">Value</span><span class="sxs-lookup"><span data-stu-id="04b9a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b9a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04b9a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="04b9a-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="04b9a-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="04b9a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04b9a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="04b9a-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="04b9a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04b9a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04b9a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="04b9a-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b9a-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b9a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="04b9a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b9a-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04b9a-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
