---
description: Especifica si el codificador está restringido por un requisito de latencia máximo.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: Propiedad MFPKEY_CONSTRAINENCLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696952"
---
# <a name="mfpkey_constrainenclatency-property"></a><span data-ttu-id="a5857-103">\_Propiedad CONSTRAINENCLATENCY de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="a5857-103">MFPKEY\_CONSTRAINENCLATENCY Property</span></span>

<span data-ttu-id="a5857-104">Especifica si el codificador está restringido por un requisito de latencia máximo.</span><span class="sxs-lookup"><span data-stu-id="a5857-104">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a5857-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a5857-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a5857-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="a5857-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="a5857-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a5857-107">Data Type</span></span>

<span data-ttu-id="a5857-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a5857-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="a5857-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a5857-109">Default Value</span></span>

<span data-ttu-id="a5857-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="a5857-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5857-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5857-111">Remarks</span></span>

<span data-ttu-id="a5857-112">Si deja esta propiedad en su valor predeterminado de **Variant \_ false**, el codificador enumera un conjunto predeterminado de modos que tienen aproximadamente 2000 milisegundos de latencia del codificador.</span><span class="sxs-lookup"><span data-stu-id="a5857-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 2000 milliseconds of encoder latency.</span></span> <span data-ttu-id="a5857-113">Si establece esta propiedad en **Variant \_ true**, también debe especificar una latencia máxima del codificador estableciendo la propiedad [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a5857-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum encoder latency by setting the [**MFPKEY\_MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) property.</span></span> <span data-ttu-id="a5857-114">En ese caso, el codificador crea modos que satisfacen el requisito de latencia y enumera solo esos modos.</span><span class="sxs-lookup"><span data-stu-id="a5857-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="a5857-115">El codificador garantiza un ejemplo de salida en cuanto el codificador ha recibido una entrada para un período de tiempo igual a **MFPKEY \_ MAXENCLATENCYMS**.</span><span class="sxs-lookup"><span data-stu-id="a5857-115">The encoder guarantees an output sample as soon as the encoder has received input for a time period equal to **MFPKEY\_MAXENCLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5857-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5857-116">Requirements</span></span>



| <span data-ttu-id="a5857-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5857-117">Requirement</span></span> | <span data-ttu-id="a5857-118">Value</span><span class="sxs-lookup"><span data-stu-id="a5857-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5857-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5857-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a5857-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a5857-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a5857-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5857-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a5857-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5857-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5857-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5857-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5857-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5857-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5857-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5857-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5857-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5857-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
