---
description: Especifica si el origen de red envía solicitudes de reenvío UDP en respuesta a los paquetes perdidos.
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: Propiedad MFNETSOURCE_RESENDSENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659841"
---
# <a name="mfnetsource_resendsenabled-property"></a><span data-ttu-id="42004-103">\_Propiedad RESENDSENABLED de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="42004-103">MFNETSOURCE\_RESENDSENABLED property</span></span>

<span data-ttu-id="42004-104">Especifica si el origen de red envía solicitudes de reenvío UDP en respuesta a los paquetes perdidos.</span><span class="sxs-lookup"><span data-stu-id="42004-104">Specifies whether the network source sends UDP resend requests in response to lost packets.</span></span>



<span data-ttu-id="42004-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="42004-105">Data type</span></span>

<span data-ttu-id="42004-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="42004-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="42004-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="42004-107">PROPVARIANT member</span></span>

<span data-ttu-id="42004-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="42004-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="42004-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="42004-109">VT\_I4</span></span>

<span data-ttu-id="42004-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="42004-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="42004-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42004-111">Remarks</span></span>

<span data-ttu-id="42004-112">La constante **MFNETSOURCE \_ RESENDSENABLED** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="42004-112">The constant **MFNETSOURCE\_RESENDSENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="42004-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="42004-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="42004-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="42004-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="42004-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="42004-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="42004-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="42004-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="42004-117">El valor predeterminado de esta propiedad es **true**.</span><span class="sxs-lookup"><span data-stu-id="42004-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="42004-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42004-118">Requirements</span></span>



| <span data-ttu-id="42004-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="42004-119">Requirement</span></span> | <span data-ttu-id="42004-120">Value</span><span class="sxs-lookup"><span data-stu-id="42004-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42004-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42004-121">Minimum supported client</span></span><br/> | <span data-ttu-id="42004-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42004-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="42004-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42004-123">Minimum supported server</span></span><br/> | <span data-ttu-id="42004-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="42004-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="42004-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42004-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="42004-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42004-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42004-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="42004-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42004-128">Registro de cliente</span><span class="sxs-lookup"><span data-stu-id="42004-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="42004-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42004-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="42004-130">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42004-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




