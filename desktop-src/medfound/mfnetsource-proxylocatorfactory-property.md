---
description: Contiene un puntero a la interfaz IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: Propiedad MFNETSOURCE_PROXYLOCATORFACTORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155557"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a><span data-ttu-id="ca3cf-103">\_Propiedad PROXYLOCATORFACTORY de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="ca3cf-103">MFNETSOURCE\_PROXYLOCATORFACTORY property</span></span>

<span data-ttu-id="ca3cf-104">Contiene un puntero a la interfaz [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="ca3cf-104">Contains a pointer to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>



<span data-ttu-id="ca3cf-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ca3cf-105">Data type</span></span>

<span data-ttu-id="ca3cf-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="ca3cf-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ca3cf-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="ca3cf-107">PROPVARIANT member</span></span>

<span data-ttu-id="ca3cf-108">**IUnknown** (puntero)</span><span class="sxs-lookup"><span data-stu-id="ca3cf-108">**IUnknown** pointer</span></span>

<span data-ttu-id="ca3cf-109">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="ca3cf-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="ca3cf-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="ca3cf-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="ca3cf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca3cf-111">Remarks</span></span>

<span data-ttu-id="ca3cf-112">La constante **MFNETSOURCE \_ PROXYLOCATORFACTORY** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ca3cf-112">The constant **MFNETSOURCE\_PROXYLOCATORFACTORY** defines the GUID for this property key.</span></span> <span data-ttu-id="ca3cf-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="ca3cf-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="ca3cf-114">Las aplicaciones pueden usar esta propiedad para proporcionar un localizador de proxy personalizado para el origen de red.</span><span class="sxs-lookup"><span data-stu-id="ca3cf-114">Applications can use this property to provide a custom proxy locator for the network source.</span></span> <span data-ttu-id="ca3cf-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="ca3cf-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="ca3cf-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="ca3cf-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca3cf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca3cf-117">Requirements</span></span>



| <span data-ttu-id="ca3cf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca3cf-118">Requirement</span></span> | <span data-ttu-id="ca3cf-119">Value</span><span class="sxs-lookup"><span data-stu-id="ca3cf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca3cf-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca3cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca3cf-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ca3cf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ca3cf-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca3cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca3cf-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca3cf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ca3cf-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca3cf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca3cf-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca3cf-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca3cf-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca3cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca3cf-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca3cf-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ca3cf-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca3cf-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="ca3cf-129">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="ca3cf-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




