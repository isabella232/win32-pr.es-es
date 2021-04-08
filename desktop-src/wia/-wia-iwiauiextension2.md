---
description: La interfaz IWiaUIExtension2 proporciona métodos que reemplazan la interfaz de usuario predeterminada proporcionada por el sistema por una interfaz de usuario personalizada y que proporcionan un icono de dispositivo personalizado.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interfaz IWiaUIExtension2 (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001183"
---
# <a name="iwiauiextension2-interface"></a><span data-ttu-id="b2351-103">Interfaz IWiaUIExtension2</span><span class="sxs-lookup"><span data-stu-id="b2351-103">IWiaUIExtension2 interface</span></span>

<span data-ttu-id="b2351-104">La interfaz IWiaUIExtension2 proporciona métodos que reemplazan la interfaz de usuario predeterminada proporcionada por el sistema por una interfaz de usuario personalizada y que proporcionan un icono de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="b2351-104">The IWiaUIExtension2 interface provides methods that replace the default, system-supplied user interface with a custom user interface, and that provide a custom device icon.</span></span> <span data-ttu-id="b2351-105">Los proveedores de dispositivos pueden implementar esta interfaz para proporcionar interfaces de usuario personalizadas para sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b2351-105">Device vendors can implement this interface to provide custom user interfaces for their devices.</span></span>

## <a name="members"></a><span data-ttu-id="b2351-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2351-106">Members</span></span>

<span data-ttu-id="b2351-107">La interfaz **IWiaUIExtension2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b2351-107">The **IWiaUIExtension2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b2351-108">**IWiaUIExtension2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b2351-108">**IWiaUIExtension2** also has these types of members:</span></span>

-   [<span data-ttu-id="b2351-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2351-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b2351-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2351-110">Methods</span></span>

<span data-ttu-id="b2351-111">La interfaz **IWiaUIExtension2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b2351-111">The **IWiaUIExtension2** interface has these methods.</span></span>



| <span data-ttu-id="b2351-112">Método</span><span class="sxs-lookup"><span data-stu-id="b2351-112">Method</span></span>                                                       | <span data-ttu-id="b2351-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2351-113">Description</span></span>                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2351-114">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="b2351-114">**DeviceDialog**</span></span>](-wia-iwiauiextension2-devicedialog.md)   | <span data-ttu-id="b2351-115">Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="b2351-115">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="b2351-116">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="b2351-116">**GetDeviceIcon**</span></span>](-wia-iwiauiextension2-getdeviceicon.md) | <span data-ttu-id="b2351-117">Obtiene un icono de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="b2351-117">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="b2351-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2351-118">Remarks</span></span>



| <span data-ttu-id="b2351-119">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2351-119">IUnknown Methods</span></span>                                        | <span data-ttu-id="b2351-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2351-120">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b2351-121">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="b2351-121">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="b2351-122">Devuelve punteros a las interfaces compatibles.</span><span class="sxs-lookup"><span data-stu-id="b2351-122">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="b2351-123">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="b2351-123">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="b2351-124">Incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="b2351-124">Increments reference count.</span></span>               |
| [<span data-ttu-id="b2351-125">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="b2351-125">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="b2351-126">Reduce el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="b2351-126">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="b2351-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2351-127">Requirements</span></span>



| <span data-ttu-id="b2351-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2351-128">Requirement</span></span> | <span data-ttu-id="b2351-129">Value</span><span class="sxs-lookup"><span data-stu-id="b2351-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2351-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2351-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b2351-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b2351-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b2351-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2351-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b2351-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2351-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b2351-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2351-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2351-135"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2351-135"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
