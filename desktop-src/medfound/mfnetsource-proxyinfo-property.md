---
description: Almacena el nombre de host y el puerto del servidor proxy que usa el origen de red.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: Propiedad MFNETSOURCE_PROXYINFO (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716345"
---
# <a name="mfnetsource_proxyinfo-property"></a><span data-ttu-id="3310d-103">\_Propiedad PROXYINFO de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="3310d-103">MFNETSOURCE\_PROXYINFO property</span></span>

<span data-ttu-id="3310d-104">Almacena el nombre de host y el puerto del servidor proxy que usa el origen de red.</span><span class="sxs-lookup"><span data-stu-id="3310d-104">Stores the host name and the port of the proxy server used by the network source.</span></span>



<span data-ttu-id="3310d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3310d-105">Data type</span></span>

<span data-ttu-id="3310d-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="3310d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3310d-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="3310d-107">PROPVARIANT member</span></span>

<span data-ttu-id="3310d-108">Cadena de caracteres anchos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="3310d-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="3310d-109">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="3310d-109">VT\_LPWSTR</span></span>

<span data-ttu-id="3310d-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="3310d-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3310d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3310d-111">Remarks</span></span>

<span data-ttu-id="3310d-112">La constante **MFNETSOURCE \_ PROXYINFO** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3310d-112">The constant **MFNETSOURCE\_PROXYINFO** defines the GUID for this property key.</span></span> <span data-ttu-id="3310d-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="3310d-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="3310d-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3310d-114">This property is read-only.</span></span> <span data-ttu-id="3310d-115">Para obtener el valor de propiedad del origen de red, llame a **IPropertyStore:: GetValue** y pase la estructura **PROPERTYKEY** en el parámetro *key* .</span><span class="sxs-lookup"><span data-stu-id="3310d-115">To get the property value from the network source, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="3310d-116">El miembro **fmtid** de **PROPERTYKEY** debe establecerse en el GUID de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3310d-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="3310d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3310d-117">Requirements</span></span>



| <span data-ttu-id="3310d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3310d-118">Requirement</span></span> | <span data-ttu-id="3310d-119">Value</span><span class="sxs-lookup"><span data-stu-id="3310d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3310d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3310d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3310d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3310d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3310d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3310d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3310d-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3310d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3310d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3310d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3310d-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3310d-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3310d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3310d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3310d-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3310d-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3310d-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3310d-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="3310d-129">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="3310d-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




