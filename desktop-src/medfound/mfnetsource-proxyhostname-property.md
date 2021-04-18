---
description: Especifica el nombre de host del servidor proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: Propiedad MFNETSOURCE_PROXYHOSTNAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715304"
---
# <a name="mfnetsource_proxyhostname-property"></a><span data-ttu-id="8adec-103">\_Propiedad PROXYHOSTNAME de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="8adec-103">MFNETSOURCE\_PROXYHOSTNAME property</span></span>

<span data-ttu-id="8adec-104">Especifica el nombre de host del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="8adec-104">Specifies the host name of the proxy server.</span></span>



<span data-ttu-id="8adec-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8adec-105">Data type</span></span>

<span data-ttu-id="8adec-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8adec-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8adec-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8adec-107">PROPVARIANT member</span></span>

<span data-ttu-id="8adec-108">Cadena de caracteres anchos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="8adec-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="8adec-109">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="8adec-109">VT\_LPWSTR</span></span>

<span data-ttu-id="8adec-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="8adec-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8adec-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8adec-111">Remarks</span></span>

<span data-ttu-id="8adec-112">La constante **MFNETSOURCE \_ PROXYHOSTNAME** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8adec-112">The constant **MFNETSOURCE\_PROXYHOSTNAME** defines the GUID for this property key.</span></span> <span data-ttu-id="8adec-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="8adec-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="8adec-114">Las aplicaciones pueden utilizar esta propiedad para configurar el localizador de proxy predeterminado al crear el objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="8adec-114">Applications can use this property to configure the default proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="8adec-115">Para establecer la propiedad, pase un puntero **IPropertyStore** en el parámetro *pProxyConfig* de la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="8adec-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="8adec-116">La aplicación debe establecer esta propiedad cuando el localizador proxy está configurado para funcionar en el modo manual.</span><span class="sxs-lookup"><span data-stu-id="8adec-116">This property must be set by the application when the proxy locator is configured to operate in the manual mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="8adec-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8adec-117">Requirements</span></span>



| <span data-ttu-id="8adec-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8adec-118">Requirement</span></span> | <span data-ttu-id="8adec-119">Value</span><span class="sxs-lookup"><span data-stu-id="8adec-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8adec-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8adec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8adec-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8adec-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8adec-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8adec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8adec-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8adec-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8adec-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8adec-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8adec-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8adec-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8adec-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8adec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8adec-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8adec-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8adec-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8adec-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="8adec-129">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="8adec-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




