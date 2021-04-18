---
description: El intervalo de puertos UDP válidos que puede usar el origen de red para recibir contenido de streaming.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: Propiedad MFNETSOURCE_UDP_PORT_RANGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715302"
---
# <a name="mfnetsource_udp_port_range-property"></a><span data-ttu-id="87488-103">\_Propiedad de \_ intervalo de puertos UDP de MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="87488-103">MFNETSOURCE\_UDP\_PORT\_RANGE property</span></span>

<span data-ttu-id="87488-104">El intervalo de puertos UDP válidos que puede usar el origen de red para recibir contenido de streaming.</span><span class="sxs-lookup"><span data-stu-id="87488-104">The range of valid UDP ports that the network source can use to receive streaming content.</span></span> <span data-ttu-id="87488-105">El valor de esta propiedad es una cadena con el formato " *m*–*n* ", donde *m* y *n* son números de puerto.</span><span class="sxs-lookup"><span data-stu-id="87488-105">The value of this property is a string with the form " *m*–*n* " where *m* and *n* are port numbers.</span></span>



<span data-ttu-id="87488-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="87488-106">Data type</span></span>

<span data-ttu-id="87488-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="87488-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="87488-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="87488-108">PROPVARIANT member</span></span>

<span data-ttu-id="87488-109">Cadena de caracteres anchos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="87488-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="87488-110">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="87488-110">VT\_LPWSTR</span></span>

<span data-ttu-id="87488-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="87488-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="87488-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87488-112">Remarks</span></span>

<span data-ttu-id="87488-113">El **intervalo de \_ \_ puertos UDP \_ constante MFNETSOURCE** define el GUID de esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="87488-113">The constant **MFNETSOURCE\_UDP\_PORT\_RANGE** defines the GUID for this property key.</span></span> <span data-ttu-id="87488-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="87488-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="87488-115">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="87488-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="87488-116">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="87488-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="87488-117">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="87488-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87488-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87488-118">Requirements</span></span>



| <span data-ttu-id="87488-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="87488-119">Requirement</span></span> | <span data-ttu-id="87488-120">Value</span><span class="sxs-lookup"><span data-stu-id="87488-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87488-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87488-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87488-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="87488-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="87488-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87488-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87488-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="87488-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="87488-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87488-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="87488-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87488-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87488-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="87488-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87488-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87488-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="87488-129">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87488-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




