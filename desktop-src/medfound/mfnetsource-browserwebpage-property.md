---
description: El valor del &\# 0034; CS (referer) &\# 0034; campo que utiliza el origen de red para el registro.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: Propiedad MFNETSOURCE_BROWSERWEBPAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e8222761299cad229b692ef400f69d0968ebd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001354"
---
# <a name="mfnetsource_browserwebpage-property"></a><span data-ttu-id="dd9df-103">\_Propiedad BROWSERWEBPAGE de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="dd9df-103">MFNETSOURCE\_BROWSERWEBPAGE property</span></span>

<span data-ttu-id="dd9df-104">El valor del campo "CS (referer)" que usa el origen de red para el registro.</span><span class="sxs-lookup"><span data-stu-id="dd9df-104">The value of the "cs(Referer)" field that the network source uses for logging.</span></span> <span data-ttu-id="dd9df-105">Las aplicaciones pueden establecer esta propiedad en la dirección URL de la página web en la que se incrustó la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dd9df-105">Applications can set this property to the URL of the webpage in which the application was embedded.</span></span>



<span data-ttu-id="dd9df-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="dd9df-106">Data type</span></span>

<span data-ttu-id="dd9df-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="dd9df-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="dd9df-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="dd9df-108">PROPVARIANT member</span></span>

<span data-ttu-id="dd9df-109">Cadena de caracteres anchos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="dd9df-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="dd9df-110">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="dd9df-110">VT\_LPWSTR</span></span>

<span data-ttu-id="dd9df-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="dd9df-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="dd9df-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd9df-112">Remarks</span></span>

<span data-ttu-id="dd9df-113">La constante **MFNETSOURCE \_ BROWSERWEBPAGE** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd9df-113">The constant **MFNETSOURCE\_BROWSERWEBPAGE** defines the GUID for this property key.</span></span> <span data-ttu-id="dd9df-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="dd9df-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="dd9df-115">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="dd9df-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="dd9df-116">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="dd9df-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="dd9df-117">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="dd9df-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd9df-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd9df-118">Requirements</span></span>



| <span data-ttu-id="dd9df-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd9df-119">Requirement</span></span> | <span data-ttu-id="dd9df-120">Value</span><span class="sxs-lookup"><span data-stu-id="dd9df-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd9df-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd9df-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dd9df-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dd9df-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dd9df-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd9df-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dd9df-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd9df-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dd9df-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd9df-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd9df-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd9df-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd9df-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd9df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd9df-128">Registro de cliente</span><span class="sxs-lookup"><span data-stu-id="dd9df-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="dd9df-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd9df-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="dd9df-130">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd9df-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




