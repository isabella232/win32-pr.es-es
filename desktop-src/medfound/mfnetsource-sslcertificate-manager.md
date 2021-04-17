---
description: Almacena el puntero IUnknown de la clase que implementa la interfaz IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: Propiedad MFNETSOURCE_SSLCERTIFICATE_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714905"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a><span data-ttu-id="9cb40-103">Propiedad del administrador de \_ SSLCERTIFICATE de MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="9cb40-103">MFNETSOURCE\_SSLCERTIFICATE\_MANAGER property</span></span>

<span data-ttu-id="9cb40-104">Almacena el puntero **IUnknown** de la clase que implementa la interfaz [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) .</span><span class="sxs-lookup"><span data-stu-id="9cb40-104">Stores the **IUnknown** pointer of the class that implements the [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) interface.</span></span> <span data-ttu-id="9cb40-105">La implementación del cliente proporciona métodos para obtener el certificado SSL del cliente cuando lo solicita el servidor.</span><span class="sxs-lookup"><span data-stu-id="9cb40-105">The client implemention provides methods to get the client SSL certificate when it is requested by the server.</span></span>



<span data-ttu-id="9cb40-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9cb40-106">Data type</span></span>

<span data-ttu-id="9cb40-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="9cb40-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9cb40-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9cb40-108">PROPVARIANT member</span></span>

<span data-ttu-id="9cb40-109">**IUnknown (puntero)**</span><span class="sxs-lookup"><span data-stu-id="9cb40-109">**IUnknown pointer**</span></span>

<span data-ttu-id="9cb40-110">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="9cb40-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="9cb40-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="9cb40-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="9cb40-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cb40-112">Remarks</span></span>

<span data-ttu-id="9cb40-113">La constante **MFNETSOURCE de \_ SSLCERTIFICATE \_ Manager** define el GUID de la clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9cb40-113">The **MFNETSOURCE\_SSLCERTIFICATE\_MANAGER** constant defines the GUID for the property key.</span></span> <span data-ttu-id="9cb40-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="9cb40-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="9cb40-115">Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="9cb40-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="9cb40-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="9cb40-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cb40-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cb40-117">Requirements</span></span>



| <span data-ttu-id="9cb40-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cb40-118">Requirement</span></span> | <span data-ttu-id="9cb40-119">Value</span><span class="sxs-lookup"><span data-stu-id="9cb40-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb40-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cb40-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9cb40-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9cb40-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9cb40-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cb40-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9cb40-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9cb40-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9cb40-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cb40-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cb40-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cb40-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cb40-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cb40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb40-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9cb40-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9cb40-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9cb40-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




