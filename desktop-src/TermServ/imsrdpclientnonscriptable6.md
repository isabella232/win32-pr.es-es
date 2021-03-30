---
title: Interfaz IMsRdpClientNonScriptable6
description: Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto. Deriva de la interfaz IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable6, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104422727"
---
# <a name="imsrdpclientnonscriptable6-interface"></a><span data-ttu-id="f281c-106">Interfaz IMsRdpClientNonScriptable6</span><span class="sxs-lookup"><span data-stu-id="f281c-106">IMsRdpClientNonScriptable6 interface</span></span>

<span data-ttu-id="f281c-107">Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f281c-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="f281c-108">Deriva de la interfaz [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) .</span><span class="sxs-lookup"><span data-stu-id="f281c-108">Derives from the [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) interface.</span></span> <span data-ttu-id="f281c-109">Solo se puede tener acceso a los métodos de esta interfaz a través de vtable; no están disponibles para los clientes con scripts.</span><span class="sxs-lookup"><span data-stu-id="f281c-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="f281c-110">Una instancia de esta interfaz se obtiene llamando a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto [**IMsTscAx**](imstscax-interface.md) y pasando **IID \_ IMsRdpClientNonScriptable6**.</span><span class="sxs-lookup"><span data-stu-id="f281c-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable6**.</span></span>

## <a name="members"></a><span data-ttu-id="f281c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f281c-111">Members</span></span>

<span data-ttu-id="f281c-112">La interfaz **IMsRdpClientNonScriptable6** hereda de [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="f281c-112">The **IMsRdpClientNonScriptable6** interface inherits from [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="f281c-113">**IMsRdpClientNonScriptable6** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f281c-113">**IMsRdpClientNonScriptable6** also has these types of members:</span></span>

- [<span data-ttu-id="f281c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f281c-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f281c-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="f281c-115">Methods</span></span>

<span data-ttu-id="f281c-116">La interfaz **IMsRdpClientNonScriptable6** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f281c-116">The **IMsRdpClientNonScriptable6** interface has these methods.</span></span>


| <span data-ttu-id="f281c-117">Método</span><span class="sxs-lookup"><span data-stu-id="f281c-117">Method</span></span>            | <span data-ttu-id="f281c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f281c-118">Description</span></span>                   |
|:-----------------------------|:-----------------|
| [<span data-ttu-id="f281c-119">**SendLocation2D**</span><span class="sxs-lookup"><span data-stu-id="f281c-119">**SendLocation2D**</span></span>](imsrdpclientnonscriptable6-sendlocation2d.md)     |  <span data-ttu-id="f281c-120">Envía un valor de latitud y longitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="f281c-120">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                   |
| [<span data-ttu-id="f281c-121">**SendLocation3D**</span><span class="sxs-lookup"><span data-stu-id="f281c-121">**SendLocation3D**</span></span>](imsrdpclientnonscriptable6-sendlocation3d.md)     | <span data-ttu-id="f281c-122">Envía un valor de latitud, longitud y altitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="f281c-122">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                 |

## <a name="requirements"></a><span data-ttu-id="f281c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f281c-123">Requirements</span></span>

| <span data-ttu-id="f281c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f281c-124">Requirement</span></span> | <span data-ttu-id="f281c-125">Value</span><span class="sxs-lookup"><span data-stu-id="f281c-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f281c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f281c-126">Minimum supported client</span></span>| <span data-ttu-id="f281c-127">Windows 10, versión 1709 (compilación 16299)</span><span class="sxs-lookup"><span data-stu-id="f281c-127">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="f281c-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f281c-128">Type library</span></span>            | <span data-ttu-id="f281c-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f281c-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f281c-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f281c-130">DLL</span></span>                  | <span data-ttu-id="f281c-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f281c-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f281c-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="f281c-132">CLSID</span></span>                    | <span data-ttu-id="f281c-133">CLSID \_ MsRdpClient12 se define como 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="f281c-133">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="f281c-134">CLSID \_ MsRdpClient12NotSafeForScripting se define como 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="f281c-134">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="f281c-135">CLSID \_ MsRdpClient11 se define como 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="f281c-135">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="f281c-136">CLSID \_ MsRdpClient11NotSafeForScripting se define como 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="f281c-136">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="f281c-137">IID</span><span class="sxs-lookup"><span data-stu-id="f281c-137">IID</span></span>                      | <span data-ttu-id="f281c-138">IID \_ IMsRdpClientNonScriptable6 se define como 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="f281c-138">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="f281c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f281c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f281c-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="f281c-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>
