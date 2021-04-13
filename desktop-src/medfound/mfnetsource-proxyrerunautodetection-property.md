---
description: Especifica si el localizador de proxy predeterminado debe forzar la detección automática del proxy.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: Propiedad MFNETSOURCE_PROXYRERUNAUTODETECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544326"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a><span data-ttu-id="1361f-103">\_Propiedad PROXYRERUNAUTODETECTION de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="1361f-103">MFNETSOURCE\_PROXYRERUNAUTODETECTION property</span></span>

<span data-ttu-id="1361f-104">Especifica si el localizador de proxy predeterminado debe forzar la detección automática del proxy.</span><span class="sxs-lookup"><span data-stu-id="1361f-104">Specifies whether the default proxy locator should force proxy auto-detection.</span></span>



<span data-ttu-id="1361f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1361f-105">Data type</span></span>

<span data-ttu-id="1361f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1361f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1361f-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1361f-107">PROPVARIANT member</span></span>

<span data-ttu-id="1361f-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="1361f-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="1361f-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1361f-109">VT\_I4</span></span>

<span data-ttu-id="1361f-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="1361f-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1361f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1361f-111">Remarks</span></span>

<span data-ttu-id="1361f-112">La constante **MFNETSOURCE \_ PROXYSETTINGS** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1361f-112">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="1361f-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="1361f-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="1361f-114">Las aplicaciones pueden utilizar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="1361f-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="1361f-115">Para establecer la propiedad, pase un puntero **IPropertyStore** en el parámetro *pProxyConfig* de la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="1361f-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="1361f-116">En el modo de detección automática, el localizador proxy utiliza el mecanismo de detección de proxy WinInet.</span><span class="sxs-lookup"><span data-stu-id="1361f-116">In auto-detect mode, the proxy locator uses the WinInet proxy detection mechanism.</span></span> <span data-ttu-id="1361f-117">Para forzar la detección automática, establezca el valor en 0.</span><span class="sxs-lookup"><span data-stu-id="1361f-117">To force auto-detection, set the value to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="1361f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1361f-118">Requirements</span></span>



| <span data-ttu-id="1361f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1361f-119">Requirement</span></span> | <span data-ttu-id="1361f-120">Value</span><span class="sxs-lookup"><span data-stu-id="1361f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1361f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1361f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1361f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1361f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1361f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1361f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1361f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1361f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1361f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1361f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1361f-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1361f-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1361f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1361f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1361f-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1361f-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1361f-129">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1361f-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="1361f-130">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="1361f-130">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




