---
description: Especifica el valor de configuración para el localizador de proxy predeterminado.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: Propiedad MFNETSOURCE_PROXYSETTINGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155556"
---
# <a name="mfnetsource_proxysettings-property"></a><span data-ttu-id="65f38-103">\_Propiedad PROXYSETTINGS de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="65f38-103">MFNETSOURCE\_PROXYSETTINGS property</span></span>

<span data-ttu-id="65f38-104">Especifica el valor de configuración para el localizador de proxy predeterminado.</span><span class="sxs-lookup"><span data-stu-id="65f38-104">Specifies the configuration setting for the default proxy locator.</span></span> <span data-ttu-id="65f38-105">El valor de esta propiedad es un miembro de la enumeración [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) .</span><span class="sxs-lookup"><span data-stu-id="65f38-105">The value of this property is a member of the [**MFNET\_PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) enumeration.</span></span>



<span data-ttu-id="65f38-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="65f38-106">Data type</span></span>

<span data-ttu-id="65f38-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="65f38-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="65f38-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="65f38-108">PROPVARIANT member</span></span>

<span data-ttu-id="65f38-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="65f38-109">**LONG**</span></span>

<span data-ttu-id="65f38-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="65f38-110">VT\_I4</span></span>

<span data-ttu-id="65f38-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="65f38-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="65f38-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65f38-112">Remarks</span></span>

<span data-ttu-id="65f38-113">La constante **MFNETSOURCE \_ PROXYSETTINGS** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="65f38-113">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="65f38-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="65f38-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="65f38-115">Las aplicaciones pueden utilizar esta propiedad para configurar el localizador proxy al crear el objeto de localizador proxy predeterminado.</span><span class="sxs-lookup"><span data-stu-id="65f38-115">Applications can use this property to configure the proxy locator when creating the default proxy locator object.</span></span> <span data-ttu-id="65f38-116">Para establecer la propiedad, pase un puntero **IPropertyStore** en el parámetro *pProxyConfig* de la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="65f38-116">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="65f38-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65f38-117">Requirements</span></span>



| <span data-ttu-id="65f38-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f38-118">Requirement</span></span> | <span data-ttu-id="65f38-119">Value</span><span class="sxs-lookup"><span data-stu-id="65f38-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65f38-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f38-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65f38-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="65f38-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="65f38-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f38-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65f38-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="65f38-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="65f38-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65f38-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65f38-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65f38-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f38-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="65f38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f38-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="65f38-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="65f38-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="65f38-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="65f38-129">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="65f38-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




