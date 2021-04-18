---
description: La interfaz IWiaUIExtension proporciona métodos que reemplazan la interfaz de usuario predeterminada del sistema, proporcionan un logotipo de mapa de bits de dispositivo personalizado y proporcionan un icono de dispositivo personalizado.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Interfaz IWiaUIExtension (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720366"
---
# <a name="iwiauiextension-interface"></a><span data-ttu-id="039d8-103">Interfaz IWiaUIExtension</span><span class="sxs-lookup"><span data-stu-id="039d8-103">IWiaUIExtension interface</span></span>

<span data-ttu-id="039d8-104">La interfaz **IWiaUIExtension** proporciona métodos que reemplazan la interfaz de usuario predeterminada del sistema, proporcionan un logotipo de mapa de bits de dispositivo personalizado y proporcionan un icono de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="039d8-104">The **IWiaUIExtension** interface provides methods that replace the default system user interface, provide a custom device bitmap logo, and provide a custom device icon.</span></span>

## <a name="members"></a><span data-ttu-id="039d8-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="039d8-105">Members</span></span>

<span data-ttu-id="039d8-106">La interfaz **IWiaUIExtension** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="039d8-106">The **IWiaUIExtension** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="039d8-107">**IWiaUIExtension** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="039d8-107">**IWiaUIExtension** also has these types of members:</span></span>

-   [<span data-ttu-id="039d8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="039d8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="039d8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="039d8-109">Methods</span></span>

<span data-ttu-id="039d8-110">La interfaz **IWiaUIExtension** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="039d8-110">The **IWiaUIExtension** interface has these methods.</span></span>



| <span data-ttu-id="039d8-111">Método</span><span class="sxs-lookup"><span data-stu-id="039d8-111">Method</span></span>                                                                  | <span data-ttu-id="039d8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="039d8-112">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="039d8-113">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="039d8-113">**DeviceDialog**</span></span>](-wia-iwiauiextension-devicedialog.md)               | <span data-ttu-id="039d8-114">Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="039d8-114">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="039d8-115">**GetDeviceBitmapLogo**</span><span class="sxs-lookup"><span data-stu-id="039d8-115">**GetDeviceBitmapLogo**</span></span>](-wia-iwiauiextension-getdevicebitmaplogo.md) | <span data-ttu-id="039d8-116">Obtiene un logotipo de mapa de bits personalizado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="039d8-116">Gets a custom bitmap logo for the device.</span></span><br/>                                         |
| [<span data-ttu-id="039d8-117">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="039d8-117">**GetDeviceIcon**</span></span>](-wia-iwiauiextension-getdeviceicon.md)             | <span data-ttu-id="039d8-118">Obtiene un icono de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="039d8-118">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="039d8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="039d8-119">Remarks</span></span>



| <span data-ttu-id="039d8-120">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="039d8-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="039d8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="039d8-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="039d8-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="039d8-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="039d8-123">Devuelve punteros a las interfaces compatibles.</span><span class="sxs-lookup"><span data-stu-id="039d8-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="039d8-124">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="039d8-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="039d8-125">Incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="039d8-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="039d8-126">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="039d8-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="039d8-127">Reduce el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="039d8-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="039d8-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="039d8-128">Requirements</span></span>



| <span data-ttu-id="039d8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="039d8-129">Requirement</span></span> | <span data-ttu-id="039d8-130">Value</span><span class="sxs-lookup"><span data-stu-id="039d8-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="039d8-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="039d8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="039d8-132">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="039d8-132">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="039d8-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="039d8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="039d8-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="039d8-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="039d8-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="039d8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="039d8-136"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-136"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
