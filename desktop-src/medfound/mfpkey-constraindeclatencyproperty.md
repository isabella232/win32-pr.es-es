---
description: Especifica si el codificador está restringido por un requisito máximo de latencia del descodificador.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: Propiedad MFPKEY_CONSTRAINDECLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696953"
---
# <a name="mfpkey_constraindeclatency-property"></a><span data-ttu-id="52393-103">\_Propiedad CONSTRAINDECLATENCY de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="52393-103">MFPKEY\_CONSTRAINDECLATENCY Property</span></span>

<span data-ttu-id="52393-104">Especifica si el codificador está restringido por un requisito máximo de latencia del descodificador.</span><span class="sxs-lookup"><span data-stu-id="52393-104">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="52393-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="52393-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="52393-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="52393-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="52393-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="52393-107">Data Type</span></span>

<span data-ttu-id="52393-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="52393-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="52393-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="52393-109">Default Value</span></span>

<span data-ttu-id="52393-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="52393-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="52393-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52393-111">Remarks</span></span>

<span data-ttu-id="52393-112">Si deja esta propiedad en su valor predeterminado de **Variant \_ false**, el codificador enumera un conjunto predeterminado de modos que tienen aproximadamente 1500 milisegundos de latencia del descodificador.</span><span class="sxs-lookup"><span data-stu-id="52393-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 1500 milliseconds of decoder latency.</span></span> <span data-ttu-id="52393-113">Si establece esta propiedad en **Variant \_ true**, también debe especificar una latencia máxima del descodificador estableciendo la propiedad [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="52393-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum decoder latency by setting the [**MFPKEY\_MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) property.</span></span> <span data-ttu-id="52393-114">En ese caso, el codificador crea modos que satisfacen el requisito de latencia y enumera solo esos modos.</span><span class="sxs-lookup"><span data-stu-id="52393-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="52393-115">El codificador garantiza que los requisitos de predesbordamiento (tamaño del búfer del descodificador) son menores o iguales que **MFPKEY \_ MAXDECLATENCYMS**.</span><span class="sxs-lookup"><span data-stu-id="52393-115">The encoder ensures that the preroll requirements (decoder buffer size) are less than or equal to **MFPKEY\_MAXDECLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="52393-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52393-116">Requirements</span></span>



| <span data-ttu-id="52393-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="52393-117">Requirement</span></span> | <span data-ttu-id="52393-118">Value</span><span class="sxs-lookup"><span data-stu-id="52393-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52393-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52393-119">Minimum supported client</span></span><br/> | <span data-ttu-id="52393-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="52393-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="52393-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52393-121">Minimum supported server</span></span><br/> | <span data-ttu-id="52393-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="52393-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52393-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52393-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="52393-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="52393-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52393-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="52393-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52393-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52393-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
