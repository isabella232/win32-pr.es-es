---
description: Especifica una lista delimitada por signos de punto y coma de servidores multimedia que pueden aceptar conexiones de aplicaciones cliente sin usar un servidor proxy.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: Propiedad MFNETSOURCE_PROXYEXCEPTIONLIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591f7036491964928937f2b48b0656e60f9a20f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716040"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a><span data-ttu-id="f70e3-103">\_Propiedad PROXYEXCEPTIONLIST de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="f70e3-103">MFNETSOURCE\_PROXYEXCEPTIONLIST property</span></span>

<span data-ttu-id="f70e3-104">Especifica una lista delimitada por signos de punto y coma de servidores multimedia que pueden aceptar conexiones de aplicaciones cliente sin usar un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="f70e3-104">Specifies a semicolon-delimited list of media servers that can accept connections from client applications without using a proxy server.</span></span>



<span data-ttu-id="f70e3-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f70e3-105">Data type</span></span>

<span data-ttu-id="f70e3-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f70e3-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f70e3-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f70e3-107">PROPVARIANT member</span></span>

<span data-ttu-id="f70e3-108">Cadena de caracteres anchos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="f70e3-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="f70e3-109">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="f70e3-109">VT\_LPWSTR</span></span>

<span data-ttu-id="f70e3-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="f70e3-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f70e3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f70e3-111">Remarks</span></span>

<span data-ttu-id="f70e3-112">La constante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f70e3-112">The constant **MFNETSOURCE\_PROXYEXCEPTIONLIST** defines the GUID for this property key.</span></span> <span data-ttu-id="f70e3-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="f70e3-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f70e3-114">Las aplicaciones pueden utilizar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="f70e3-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="f70e3-115">Para establecer la propiedad, pase un puntero **IPropertyStore** en el parámetro *pProxyConfig* de la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="f70e3-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="f70e3-116">El localizador proxy no realiza la detección de proxy para estas direcciones.</span><span class="sxs-lookup"><span data-stu-id="f70e3-116">The proxy locator does not perform proxy detection for these addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70e3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f70e3-117">Requirements</span></span>



| <span data-ttu-id="f70e3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f70e3-118">Requirement</span></span> | <span data-ttu-id="f70e3-119">Value</span><span class="sxs-lookup"><span data-stu-id="f70e3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f70e3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f70e3-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f70e3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f70e3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f70e3-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f70e3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f70e3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f70e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f70e3-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f70e3-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70e3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f70e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70e3-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f70e3-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f70e3-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f70e3-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f70e3-129">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="f70e3-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




