---
description: El valor del campo &\# 0034; c-hostexe&\# 0034; que usa el origen de red para el registro.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: Propiedad MFNETSOURCE_HOSTEXE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817123"
---
# <a name="mfnetsource_hostexe-property"></a><span data-ttu-id="c9538-103">\_Propiedad HOSTEXE de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="c9538-103">MFNETSOURCE\_HOSTEXE property</span></span>

<span data-ttu-id="c9538-104">El valor del campo "c-hostexe" que usa el origen de red para el registro.</span><span class="sxs-lookup"><span data-stu-id="c9538-104">The value of the "c-hostexe" field that the network source uses for logging.</span></span> <span data-ttu-id="c9538-105">Las aplicaciones pueden establecer esta propiedad en el nombre de la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="c9538-105">Applications can set this property to the name of the host application.</span></span> <span data-ttu-id="c9538-106">Por ejemplo, el valor podría ser "iexplore.exe" si la aplicación se hospeda en una página web.</span><span class="sxs-lookup"><span data-stu-id="c9538-106">For example, the value could be "iexplore.exe" if the application is hosted in a webpage.</span></span>



<span data-ttu-id="c9538-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c9538-107">Data type</span></span>

<span data-ttu-id="c9538-108">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="c9538-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c9538-109">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="c9538-109">PROPVARIANT member</span></span>

<span data-ttu-id="c9538-110">Cadena de caracteres anchos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="c9538-110">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="c9538-111">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="c9538-111">VT\_LPWSTR</span></span>

<span data-ttu-id="c9538-112">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="c9538-112">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c9538-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9538-113">Remarks</span></span>

<span data-ttu-id="c9538-114">La constante **MFNETSOURCE \_ HOSTEXE** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9538-114">The constant **MFNETSOURCE\_HOSTEXE** defines the GUID for this property key.</span></span> <span data-ttu-id="c9538-115">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="c9538-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="c9538-116">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="c9538-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="c9538-117">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="c9538-117">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="c9538-118">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c9538-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9538-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9538-119">Requirements</span></span>



| <span data-ttu-id="c9538-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9538-120">Requirement</span></span> | <span data-ttu-id="c9538-121">Value</span><span class="sxs-lookup"><span data-stu-id="c9538-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9538-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9538-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9538-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9538-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c9538-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9538-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9538-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9538-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c9538-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9538-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9538-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9538-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9538-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9538-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9538-129">Registro de cliente</span><span class="sxs-lookup"><span data-stu-id="c9538-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="c9538-130">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9538-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c9538-131">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9538-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




