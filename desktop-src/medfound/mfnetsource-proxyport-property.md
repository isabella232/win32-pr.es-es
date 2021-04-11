---
description: Especifica el número de puerto del servidor proxy.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: Propiedad MFNETSOURCE_PROXYPORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275940"
---
# <a name="mfnetsource_proxyport-property"></a><span data-ttu-id="9d4dd-103">MFNETSOURCE \_ propiedad PROXYPORT</span><span class="sxs-lookup"><span data-stu-id="9d4dd-103">MFNETSOURCE\_PROXYPORT property</span></span>

<span data-ttu-id="9d4dd-104">Especifica el número de puerto del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="9d4dd-104">Specifies the port number of the proxy server.</span></span>



<span data-ttu-id="9d4dd-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9d4dd-105">Data type</span></span>

<span data-ttu-id="9d4dd-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="9d4dd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9d4dd-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9d4dd-107">PROPVARIANT member</span></span>

<span data-ttu-id="9d4dd-108">**DWORD** (almacenado como **Long**)</span><span class="sxs-lookup"><span data-stu-id="9d4dd-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="9d4dd-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9d4dd-109">VT\_I4</span></span>

<span data-ttu-id="9d4dd-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="9d4dd-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="9d4dd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d4dd-111">Remarks</span></span>

<span data-ttu-id="9d4dd-112">La constante **MFNETSOURCE \_ PROXYPORT** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9d4dd-112">The constant **MFNETSOURCE\_PROXYPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="9d4dd-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="9d4dd-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="9d4dd-114">Las aplicaciones pueden utilizar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="9d4dd-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="9d4dd-115">Para establecer la propiedad, pase un puntero **IPropertyStore** en el parámetro *pProxyConfig* de la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="9d4dd-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="9d4dd-116">Si esta propiedad no está establecida para HTTP, el localizador proxy utiliza de forma predeterminada el valor 80.</span><span class="sxs-lookup"><span data-stu-id="9d4dd-116">If this property is not set for HTTP, then by default the proxy locator uses a value of 80.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d4dd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d4dd-117">Requirements</span></span>



| <span data-ttu-id="9d4dd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d4dd-118">Requirement</span></span> | <span data-ttu-id="9d4dd-119">Value</span><span class="sxs-lookup"><span data-stu-id="9d4dd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4dd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d4dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9d4dd-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9d4dd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9d4dd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d4dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9d4dd-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d4dd-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9d4dd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d4dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d4dd-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d4dd-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d4dd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d4dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d4dd-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9d4dd-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9d4dd-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9d4dd-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="9d4dd-129">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="9d4dd-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




