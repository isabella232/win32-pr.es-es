---
description: Especifica si el localizador de proxy debe utilizar un servidor proxy para las direcciones locales.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: Propiedad MFNETSOURCE_PROXYBYPASSFORLOCAL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808047"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a><span data-ttu-id="ca82c-103">\_Propiedad PROXYBYPASSFORLOCAL de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="ca82c-103">MFNETSOURCE\_PROXYBYPASSFORLOCAL property</span></span>

<span data-ttu-id="ca82c-104">Especifica si el localizador de proxy debe utilizar un servidor proxy para las direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="ca82c-104">Specifies whether the proxy locator should use a proxy server for local addresses.</span></span>



<span data-ttu-id="ca82c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ca82c-105">Data type</span></span>

<span data-ttu-id="ca82c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="ca82c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ca82c-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="ca82c-107">PROPVARIANT member</span></span>

<span data-ttu-id="ca82c-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="ca82c-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="ca82c-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ca82c-109">VT\_I4</span></span>

<span data-ttu-id="ca82c-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="ca82c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="ca82c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca82c-111">Remarks</span></span>

<span data-ttu-id="ca82c-112">La constante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ca82c-112">The constant **MFNETSOURCE\_PROXYBYPASSFORLOCAL** defines the GUID for this property key.</span></span> <span data-ttu-id="ca82c-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="ca82c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="ca82c-114">Las aplicaciones pueden utilizar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="ca82c-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="ca82c-115">Para establecer la propiedad, pase un puntero **IPropertyStore** en el parámetro *pProxyConfig* de la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="ca82c-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="ca82c-116">El valor debe establecerse en 0 si el servidor proxy se va a usar para las direcciones locales; de lo contrario, un valor distinto de cero configura el localizador de proxy predeterminado para omitir el servidor proxy para las direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="ca82c-116">The value must be set to 0 if the proxy server is to be used for local addresses; otherwise a nonzero value configures the default proxy locator to skip the proxy server for local addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca82c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca82c-117">Requirements</span></span>



| <span data-ttu-id="ca82c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca82c-118">Requirement</span></span> | <span data-ttu-id="ca82c-119">Value</span><span class="sxs-lookup"><span data-stu-id="ca82c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca82c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca82c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca82c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ca82c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ca82c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca82c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca82c-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca82c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ca82c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca82c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca82c-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca82c-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca82c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca82c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca82c-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca82c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ca82c-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca82c-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="ca82c-129">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="ca82c-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




